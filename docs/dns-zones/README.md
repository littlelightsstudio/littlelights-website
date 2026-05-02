# DNS Zone Files für Hetzner-Import

Eine BIND-Zone-Datei pro Domain. Wird in Hetzner Cloud Console über **DNS → Add DNS zone → Import zone file** hochgeladen.

## Workflow für jede Domain

1. Bei easyname Screenshot der DNS-Zone und des Email-Tabs machen
2. dig-Scan über die Domain für Public-DNS-Vergleich
3. Cleanup-Entscheidungen treffen (siehe unten)
4. Zone-File hier ablegen als `<domain>.zone`
5. In Hetzner importieren (zero-Risk, wirkt nicht live bis Nameserver bei easyname umgestellt werden)
6. Verifikations-dig gegen Hetzner-Nameserver (`dig @helium.ns.hetzner.de ...`)
7. Erst NACH Verifikation aller Zonen: Cutover-Phase bei easyname (separat, eine Domain nach der anderen)

## Cleanup-Konventionen (für alle easyname-Domains)

Diese Records werden beim Migrieren systematisch entfernt:

| Record | Begründung |
|---|---|
| `ftp.<domain>` A-Record | Kein FTP-Server in Betrieb |
| `webmail.<domain>` A-Record | Webmail wird nicht genutzt |
| `mail.<domain>` A-Record | Pointer auf easyname-Hosting, ungenutzt |
| `autodiscover.<domain>` CNAME | Outlook-Auto-Konfig, nicht im Einsatz |
| `autoconfig.<domain>` CNAME | Thunderbird-Auto-Konfig, nicht im Einsatz |
| `*.<domain>` Wildcard A | Ohne konkreten Use Case raus, sauberer |

**Bedingt behalten** (pro Domain entscheiden):

| Record | Wann behalten |
|---|---|
| `MX` Records | Wenn aktives Forwarding bei easyname konfiguriert ist (Email-Tab prüfen) |
| `TXT v=spf1` | Behalten wenn MX bleibt (zusammenhängend) |
| `easyname._domainkey` CNAME | Behalten wenn MX bleibt (zusammenhängend) |
| Root `A` + `www` `A` | Behalten wenn Browser-Anzeige gewünscht (Default-easyname-Page o.ä.) |

**Sonderfall Google-Workspace-Domains** (4 Stück: littlelights.studio, littlelightsstudio.at, littlelightsstudio.com, michaelsokolar.com):
- Andere MX-Records (`smtp.google.com`)
- Andere DKIM-Selectoren
- Google-Verifications (TXT records mit `google-site-verification=...`)
- Hier 1:1 übernehmen, nicht aufräumen

**Sonderfall komplexe Legacy-Domains** (z.B. sokolar.com, michaelsokolar.com, evtl. helenaflinn.com):

Solche Domains haben über Jahre gewachsene Konfigurationen mit:
- Vielen aktiven Subdomains (nicht nur ftp/mail/webmail), darunter manche mit Fremd-IPs (Home-Server etc.)
- HTTP-Redirects pro Subdomain (in easyname's "Subdomains/Weiterleitungen"-Tab konfiguriert, NICHT in DNS sichtbar)
- Vielen Email-Forwarding-Aliases (alle gehen letztlich an Gmail/Google Workspace)

**Wichtige Klarstellung — keine echten Mailboxen mehr:** Trotz `10974mailX`-IDs in easyname's Email-Tab gibt es **keine echten Mailboxen** mehr in Betrieb. Alles läuft über Forwarding zu Gmail oder Google Workspace. Die IDs sind easyname-interne Forwarding-Slots, kein Mailbox-State der bei der Migration mitgenommen werden müsste.

**Wichtig zu verstehen:**

| Easyname-Feature | DNS-Sichtbarkeit | Funktioniert nach DNS-Migration? |
|---|---|---|
| Email-Forwarding (alle Aliases) | nicht in DNS | Ja, solange MX → easyname zeigt |
| HTTP-Redirect / Subdomain-Weiterleitung | nicht in DNS | Ja, solange A-Record → 77.244.243.39 (oder ähnliche easyname-IP) zeigt |
| Webspace mit PHP | nicht in DNS | Ja, solange A-Record → easyname-IP zeigt |
| Subdomain mit Fremd-IP (Home-Server etc.) | A-Record sichtbar | Ja, A-Record 1:1 in Hetzner-Zone übernehmen |

D.h. **wenn wir A-Records auf easyname-IP belassen und MX auf easyname-MX-Server**, funktionieren alle diese Features auch nach DNS-Migration weiter — easyname's Hosting-Layer kümmert sich darum.

**Workflow für komplexe Domains:**

1. **Domain-für-Domain durchgehen mit User**, nicht in Bulk. User klassifiziert pro Subdomain und pro Forwarding-Alias:

   | Item | User-Entscheidung |
   |---|---|
   | jede Subdomain einzeln | behalten (aktiv genutzt) / entfernen (veraltet) / unsicher (→ behalten) |
   | jeder Email-Forwarding-Alias | gleich |

2. **Subdomains mit Fremd-IPs** (z.B. Home-Server `81.217.59.225`) immer behalten und 1:1 übernehmen — das sind echte Services.
3. **Bei klarem "nein": nicht in Zone-File aufnehmen.** Easyname-Redirect-Regeln verwaisen dann harmlos, Subdomain wird NXDOMAIN nach Cutover.
4. **MX bleibt erhalten solange ≥1 aktiver Forwarding-Alias** existiert.

## Was bei Hetzner-Import automatisch ergänzt wird

- **SOA**-Record (Hetzner generiert eigenen)
- **NS**-Records (Hetzners 3 Nameserver: helium, hydrogen, oxygen)

Daher in den Zone-Files weder SOA noch NS eintragen — nur Inhalts-Records.

## TTL-Strategie

- **Zone-File-Default:** 3600 (1 Stunde) für alle Records
- **Direkt vor Cutover bei easyname:** in Hetzner alle Records auf TTL **300** runter (5 Min) für schnelles Rollback-Fenster
- **24-48h nach erfolgreichem Cutover:** TTLs zurück auf 3600

## Format-Hinweise

- `@` = Root-Domain (= `$ORIGIN`)
- Bare names (`www`, `mail`) = relativ zu `$ORIGIN`, also `www.<domain>`
- FQDNs mit trailing dot (`mx01.easyname.eu.`) = absolut, kein `$ORIGIN` angehängt
- TXT-Werte in Anführungszeichen (BIND-Standard)
- Comments mit `;`

## Status-Tracker pro Zone-File

Pro Domain in [`../domain-migration.md`](../domain-migration.md) Status nachpflegen:
- `Zone-File generiert` (`.zone` liegt hier)
- `In Hetzner importiert` (Zone in Hetzner sichtbar)
- `Verified gegen NS` (dig @hetzner-ns ergibt korrekte Records)
- `Cutover bei easyname erfolgt`
- `Stabil` (24h+ ohne Issues)

## Existierende Zone-Files

**Stand 27.04.2026:** alle 21 Zones generiert. sokolar.com mit konservativer 1:1-Migration (Subdomain-Cleanup wird separate Session, Zone-File aber jetzt schon einsatzbereit für Hetzner-Import).

| File | Status | Besonderheit |
|---|---|---|
| `nocturnedomains.com.zone` | ✅ in Hetzner importiert, NS verifiziert, Cutover ausstehend | Pilot, vor Cleanup-Konventionen |
| `sokolar.at.zone` | ✅ generiert | Cleanup-Pilot |
| `brand-film.agency.zone` | ✅ generiert | Brand-Schutz (Standard-Cleanup) |
| `brandfilm.agency.zone` | ✅ generiert | Brand-Schutz (Standard-Cleanup) |
| `helenaflinn-chronicles.com.zone` | ✅ generiert | Brand-Schutz (Standard-Cleanup) |
| `littlelights.agency.zone` | ✅ generiert | Brand-Schutz (Standard-Cleanup) |
| `littlelights.at.zone` | ✅ generiert | Brand-Schutz (Standard-Cleanup) |
| `littlelights.media.zone` | ✅ generiert | Brand-Schutz (Standard-Cleanup) |
| `littlelights.productions.zone` | ✅ generiert | Brand-Schutz (Standard-Cleanup) |
| `littlelights.pub.zone` | ✅ generiert | Brand-Schutz (Standard-Cleanup) |
| `michaelsokolar.at.zone` | ✅ generiert | Brand-Schutz (Standard-Cleanup) |
| `nocturnecodex.com.zone` | ✅ generiert | Helena-World-Reserve (Standard-Cleanup) |
| `littlelights-studio.at.zone` | ✅ generiert | Brand-Schutz, kein AAAA |
| `littlelights-studio.com.zone` | ✅ generiert | Brand-Schutz, kein AAAA |
| `ferienwohnung-mistelbach.at.zone` | ✅ generiert | WordPress-Hosting, **keine Mail-Records** |
| `helenaflinn.com.zone` | ✅ generiert | GitHub Pages + easyname Mail |
| `michaelsokolar.com.zone` | ✅ generiert | Google + GitHub + MailerLite + DKIM + DMARC |
| `littlelightsstudio.at.zone` | ✅ generiert | Google Workspace + DKIM + DMARC |
| `littlelightsstudio.com.zone` | ✅ generiert | Google Workspace + User-Triage + DKIM + DMARC |
| `littlelights.studio.zone` | ✅ generiert | **Geschäftskritisch** — Google + MS + Subdomain-Cluster + DKIM + DMARC + Cross-Domain-Auth |
| `sokolar.com.zone` | ✅ generiert (konservativ 1:1) | komplexes Legacy — alle Subdomains 1:1 übernommen, Subdomain-Cleanup deferred
