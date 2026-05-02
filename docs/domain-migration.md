# Domain-Migration: easyname → Hetzner

Lebende Datei. Zwei-Phasen-Modell für den Umzug aller Domains von easyname zu Hetzner. Status-Tracker pro Domain ganz unten — bei jedem Schritt aktualisieren.

---

## Update 27.04.2026 (Nachmittag) — Phase 4b gestartet

**Drop-Entscheidung getroffen.** 5 Domains werden NICHT migriert, sondern bei easyname auslaufen gelassen:

- `brand-film.agency` (€43.20/Jahr) — Doppelung mit `brandfilm.agency`
- `brandfilm.agency` (€43.20/Jahr) — Doppelung mit `brand-film.agency`, eine reicht; `littlelights.agency` deckt Brand-Schutz für Hauptmarke ab
- `littlelights.pub` (€58.80/Jahr) — .pub als Publishing-TLD nicht intuitiv, niemand assoziiert es richtig
- `littlelights-studio.at` (€13.20/Jahr) — Bindestrich-Variante zu `littlelightsstudio.at`, in 2026 kein realer Tippschutz mehr
- `littlelights-studio.com` (€16.20/Jahr) — Bindestrich-Variante zu `littlelightsstudio.com`

**Ersparnis: €174.60/Jahr.** Verbleibendes Portfolio: **16 Domains.**

**Registrar-Entscheidung:** Hetzner Domains via konsoleH. Single-Provider-Lösung gewählt trotz ~€185/Jahr Aufpreis gegenüber INWX-Schätzung — Operations-Einfachheit wertvoller als die Ersparnis. Server bleibt sowieso Hetzner Cloud, Risiko-Streuung Server ≠ Registrar-Account akzeptiert.

**Hetzner Domains funktioniert über konsoleH.** Es gibt keinen Standalone-Domain-Service à la Cloudflare Registrar oder Porkbun. Das Produkt heisst „Domains → Registration only" und wird in [konsoleh.hetzner.com](https://konsoleh.hetzner.com) verwaltet, bestellt über [accounts.hetzner.com](https://accounts.hetzner.com).

**Pilot-Pivot:** Ursprünglich war `nocturnecodex.com` als Pilot vorgesehen. Wegen ICANN-60-Tage-Lock (Domain wurde innerhalb der letzten 60 Tage registriert oder transferiert) ist der Registrar-Transfer aktuell blockiert. Stattdessen läuft jetzt der Pilot mit **`nocturnedomains.com`**:

- 27.04.2026 Nachmittag: Auth-Code bei easyname geholt, Transfer-Lock entfernt (verifiziert via WHOIS: `Domain Status: ok`)
- 27.04.2026 Nachmittag: Transfer bei Hetzner via konsoleH initiiert mit den 3 Hetzner-DNS-NS in Advanced options
- Status: „being processed" in konsoleH (manuelles Hetzner-Mitarbeiter-Review läuft)
- ICANN-Bestätigungsmail: erwartet an WHOIS-Owner-Mail
- Erwartete Abschluss-Dauer: 5-7 Tage

**NS-Cutover für `nocturnedomains.com` erfolgt automatisch mit dem Transfer**, weil die 3 Hetzner-NS direkt in der Transfer-Form spezifiziert wurden (Hetzner-DNS-Zone war seit dem 27.04.2026 importiert und verifiziert). Damit fallen DNS-Cutover und Registrar-Transfer in einem Schritt zusammen — klassisches Anti-Pattern, in diesem Fall vertretbar weil die Domain ungenutzt ist und Downtime-Toleranz hoch.

**`nocturnecodex.com` Status:**
- DNS bei Hetzner ✅ (Cutover seit 27.04.2026 morgens)
- Registrar bei easyname (Lock-blockiert, Transfer wartet auf Ablauf der 60 Tage)
- Follow-up nötig: in ~30-60 Tagen Transfer erneut versuchen

**Nächste Schritte nach Pilot-Erfolg:**
1. Pilot-Abschluss `nocturnedomains.com` abwarten (5-7 Tage)
2. Bei Erfolg: restliche 14 Domains nach und nach transferieren (Reihenfolge: weitere Brand-Schutz zuerst, Mission-critical zuletzt)
3. `nocturnecodex.com` nachziehen sobald 60-Tage-Lock fällt

**Geschätzte Gesamtkosten Hetzner Domains (16 Domains): €411.00/Jahr**

| TLD | Anzahl | × Preis | Summe |
|---|---|---|---|
| .com | 7 | €16.20 | €113.40 |
| .at | 5 | €13.20 | €66.00 |
| .studio | 1 | €63.60 | €63.60 |
| .agency | 1 | €43.20 | €43.20 |
| .media | 1 | €66.00 | €66.00 |
| .productions | 1 | €58.80 | €58.80 |

(Hinweis: `.com` zeigte in der konkreten Transfer-Form €13.50 statt €16.20 aus der Preisliste — vermutlich netto/brutto-Unterschied, real-bezahlte Summen können marginal abweichen.)

---

## Aktueller Stand (Session 27.04.2026)

**Strategie-Entscheidung:** Wir bauen **zuerst alle 21 Hetzner-Zonen komplett auf** (zero-Risk, wirkt nicht live), verifizieren jede gegen Hetzners Nameserver, und cutovern erst danach kontrolliert eine Domain nach der anderen bei easyname. Begründung: Bulk-Aufbau ist effizienter, erlaubt Konsistenz-Checks zwischen den Zonen, und der Cutover wird stressfrei.

**Cleanup beim Migrieren:** Konventionen festgelegt in [`dns-zones/README.md`](dns-zones/README.md). Systematisch entfernt: `ftp`, `webmail`, `mail`, `autodiscover`, `autoconfig`, Wildcard. Bedingt: `MX`/`SPF`/`DKIM` (zusammenhängend, je Domain entschieden basierend auf Forwarding-Aktivität bei easyname).

**Was schon erledigt ist:**

- ✅ DNS-Scan über alle 21 Domains (alle haben aktive Mail-Konfig, 17 easyname / 4 Google Workspace)
- ✅ Erste Pilot-Zone `nocturnedomains.com` in Hetzner importiert + verifiziert (Cutover bei easyname noch nicht gemacht)
- ✅ Cleanup-Konventionen etabliert (siehe [`dns-zones/README.md`](dns-zones/README.md))
- ✅ Triage-Runde mit User durchgeführt ([`dns-zones/triage.md`](dns-zones/triage.md))
- ✅ DKIM-Werte für 4 Google-Workspace-Domains aus Google Admin Console gesammelt
- ✅ **Zone-Files für alle 21 Domains generiert** (sokolar.com konservativ 1:1, Subdomain-Cleanup separate Session)
- ✅ **Alle 21 Zonen in Hetzner DNS importiert** (27.04.2026, Record-Counts verifiziert)
- ✅ **Erster Cutover:** `nocturnecodex.com` NS bei easyname auf Hetzner umgestellt (27.04.2026)
- 🤖 **Verifikations-Routine** geplant für 2026-04-29 10:00 (Vienna): Zone-Integrity gegen helium.ns.hetzner.de + NS-Propagation aller 21 Domains
  - 12 Standard-Bulk-Domains (Brand-Schutz, identisches easyname-Schema)
  - ferienwohnung-mistelbach.at (WordPress-Sonderfall, ohne Mail-Records)
  - helenaflinn.com (GitHub Pages + easyname Mail)
  - 4 Google-Workspace-Domains mit DKIM + DMARC ergänzt (Cross-Domain-Auth auf littlelights.studio)
  - sokolar.at (Pilot-Cleanup) und nocturnedomains.com (Pilot, schon importiert)

**Was als Nächstes ansteht:**

1. **2026-04-29 10:00:** Verifikations-Routine läuft automatisch durch alle 21 Zonen — Output prüfen, Mismatches (falls vorhanden) korrigieren
2. **Cutover-Phase fortsetzen:** Brand-Schutz-Domains in Batches NS bei easyname umstellen, je 24h beobachten. Empfohlene Reihenfolge: nocturnedomains.com (Pilot, schon in Hetzner) → restliche Brand-Schutz-Bulk → ferienwohnung-mistelbach.at → helenaflinn-Reihe → Google-Workspace-Domains einzeln mit Pause → littlelights.studio ganz zum Schluss
3. **sokolar.com Subdomain-Cleanup-Session** (separate Session, optional vor oder nach Cutover): Subdomain für Subdomain mit User durchgehen, Karteileichen aussortieren

**Komplexe Legacy-Domains** (mind. sokolar.com bestätigt, vermutlich auch michaelsokolar.com und helenaflinn.com): brauchen Triage-Gespräch vor Zone-Generation. Easyname hat HTTP-Redirects + Webspace + Forwardings ausserhalb DNS, die nur funktionieren wenn A-Records weiterhin auf easyname-IP zeigen und MX bei easyname bleibt. Details + Workflow in [`dns-zones/README.md`](dns-zones/README.md).

**WordPress-Sonderfall:** Eine der Domains hostet eine aktive WordPress-Installation auf easyname's Webspace. Die DNS-Migration berührt das nicht — solange der A-Record nach der Migration weiter auf die easyname-IP zeigt, läuft WordPress unverändert weiter. Der eigentliche WordPress-Umzug (Files + MySQL-DB auf neuen Host, dann A-Record umlenken) ist ein **eigenes separates Projekt**, nicht Teil dieser DNS-Migration. User klärt im neuen Chat welche Domain das ist.

**Wichtige Cleanup-Pattern für die Bulk-Phase:**

| Domain-Typ | Records die wir behalten | Records die raus |
|---|---|---|
| **Brand-Schutz, kein Forwarding** | A root, A www | alles Mail-bezogene, Sub-A, Wildcard, autoconfig/autodiscover |
| **Forwarding-Domain (easyname)** | A root, A www, MX (×2), SPF, DKIM-CNAME | autoconfig, autodiscover, FTP, mail, webmail, Wildcard |
| **Google Workspace** | komplett anders (siehe README), 1:1 übernehmen | nur unbenutzte Subdomains aufräumen |

Die Forwarding-Aktivität pro Domain klärt sich aus dem Email-Tab-Screenshot bei easyname.

---

## Warum zwei Phasen

Eine Domain-Migration hat zwei voneinander unabhängige Risiken:

1. **DNS-Risiko:** Wenn ein Record (besonders MX, SPF, DKIM, DMARC) falsch übernommen wird, fallen Mails aus oder gehen in den Spam.
2. **Registrar-Risiko:** Während des 5-7-tägigen Transferfensters ist die Domain in einem Übergangszustand. Auth-Code-Probleme, ICANN-Verifikation, Ablauf-Konflikte können die Domain temporär lahmlegen.

Wenn beide Risiken gleichzeitig schlagen, ist Debugging die Hölle: Liegt's am DNS? Am Registrar? Du hast keinen sauberen Anhaltspunkt mehr.

**Phase 1 (DNS only) ist innerhalb von Minuten zurückrollbar** — Nameserver bei easyname wieder auf easyname-Default umstellen, fertig. Phase 2 (Registrar) kommt erst nach mehreren Wochen sauberem DNS-Betrieb. So testen wir jede Komponente isoliert.

---

## Phase 1: DNS-Migration

**Was passiert:** Domain bleibt bei easyname registriert. DNS-Records werden in Hetzner DNS gepflegt. Bei easyname stellen wir nur die Nameserver auf Hetzners NS um.

**Vorbereitung pro Domain:**

1. **Aktuelle DNS-Zone bei easyname dokumentieren.** Screenshot oder Liste aller Records:
   - **A** und **AAAA**: alle IP-Verweise (Root-Domain, www, Subdomains)
   - **MX**: alle Mail-Server (Google: 5 Einträge mit unterschiedlichen Prios; Forwarding: meist 1 Eintrag)
   - **TXT**: SPF, DKIM (`google._domainkey.<domain>`), DMARC (`_dmarc.<domain>`), Site-Verifications (Google, Microsoft, Stripe etc.)
   - **CNAME**: Subdomain-Aliase (häufig `www`, Mail-Tracking, App-Verweise)
   - **CAA**: SSL-Zertifikat-Authority-Beschränkungen (oft leer)
   - **SRV**: nur falls Voice/Chat-Services über die Domain laufen

2. **TTL bei easyname herabsetzen.** Mind. 24h vor der Umstellung alle Record-TTLs auf **300 Sekunden** (5 Min) stellen. Sonst hängen alte Werte stundenlang im DNS-Cache wenn was nicht stimmt und du korrigieren willst.

**Migrations-Schritte (Hetzner Cloud Console → DNS):**

1. **Add DNS zone** → Domain-Name eintragen (z.B. `sokolar.com`) → Zone wird angelegt
2. **Alle Records aus der easyname-Liste 1:1 nachbauen.** Wichtig:
   - Bei MX: gleicher Hostname und gleiche Priorität wie bei easyname
   - Bei TXT: kompletten Wert in Anführungszeichen kopieren (besonders bei langen DKIM-Keys)
   - TTL erstmal auf 3600 (1 Stunde) lassen
3. **Hetzner-Nameserver notieren.** In der Zone werden 3 angezeigt:
   - `helium.ns.hetzner.de`
   - `hydrogen.ns.hetzner.com`
   - `oxygen.ns.hetzner.com`
4. **Bei easyname:** Domain-Verwaltung → Nameserver → Default-NS durch die 3 Hetzner-NS ersetzen, speichern
5. **Warten** — DNS-Propagation typischerweise 15 Min bis 2 Std, im Worst Case 24h
6. **Verifizieren** mit folgenden Befehlen:

```bash
# Nameserver propagiert?
dig NS sokolar.com +short
# Erwartet: hetzner-namen statt easyname-namen

# A-Records OK?
dig A sokolar.com +short

# MX-Records OK? KRITISCH bei Email-Domains
dig MX sokolar.com +short

# TXT-Records OK? (SPF, DMARC)
dig TXT sokolar.com +short

# DKIM separat (Selector "google" für Google Workspace)
dig TXT google._domainkey.sokolar.com +short
```

7. **Email-Test:** Eine Mail von externem Account an `<beliebig>@<domain>` schicken. Sollte ohne Verzögerung ankommen. **Auch ausgehende Mail testen** (von einer Adresse auf der Domain an einen externen Account schicken).

8. **24h beobachten.** Wenn alles ruhig läuft: Phase 1 für diese Domain abgeschlossen.

---

## Phase 2: Registrar-Transfer

**Erst beginnen wenn alle Domains mindestens 2-4 Wochen stabil in Phase 1 laufen.**

**Vorbereitung:**

- Sicherstellen dass Owner-Kontaktdaten bei easyname aktuell sind (E-Mail, Adresse, Telefon)
- Domain darf in den letzten 60 Tagen nicht registriert oder transferiert worden sein
- Domain-Lock entfernen
- Auth-Code (EPP-Code, Transfer-Key) bei easyname anfordern

**Bei Hetzner Domains:**

1. Im Hetzner Account → "Domains" → "Transfer Domain"
2. Domain-Name + Auth-Code eingeben
3. Renewal-Gebühr für 1 Jahr zahlen
4. Bestätigungsmail an Owner-Kontakt → Link klicken (ICANN-Verifikation, kommt fast immer)
5. **5-7 Tage warten** — Domain funktioniert die ganze Zeit normal weiter
6. Nach Abschluss: Domain ist bei Hetzner registriert, DNS bleibt unverändert auf den Hetzner-Nameservern (wenn Phase 1 schon gemacht ist)

**Stolperfallen:**

- ICANN-Verification-Mail unbedingt klicken — wenn ignoriert, wird die Domain nach 15 Tagen suspendiert
- Bei `.studio`, `.com`, `.org` ist Auth-Code-Format alphanumerisch; bei `.de` ist es ein DENIC-AuthInfo
- Falls Hetzner Domains die Domain-Endung nicht unterstützt (selten), bleibt die Domain bei easyname; nur DNS auf Hetzner

---

## Rollback-Plan

### Phase 1 zurückrollen (DNS-Notfall)

Wenn nach Nameserver-Wechsel zu Hetzner irgendwas crasht:

1. **Bei easyname:** Nameserver wieder auf easyname-Default zurückstellen
2. Innerhalb von Minuten ist die alte easyname-DNS-Zone wieder aktiv
3. Hetzner-Zone bleibt zur späteren Korrektur stehen

Voraussetzung: easyname-DNS-Zone wurde NICHT bei easyname gelöscht. Daher bei Phase 1 die Records bei easyname stehen lassen, nur die NS umstellen.

### Phase 2 zurückrollen (Registrar-Notfall)

Schwieriger: nach abgeschlossenem Transfer kann die Domain frühestens nach 60 Tagen erneut transferiert werden. Daher Phase 2 nur starten wenn Phase 1 wirklich stabil ist.

---

## Was bei Email-Domains besonders zu beachten

### Google Workspace (littlelights.studio, michaelsokolar.com)

Folgende Records müssen 1:1 übernommen werden:

- **MX (5 Einträge):**
  - Priority 1: `smtp.google.com`
  - Priority 5: `alt1.smtp.google.com`
  - Priority 5: `alt2.smtp.google.com`
  - Priority 10: `alt3.smtp.google.com`
  - Priority 10: `alt4.smtp.google.com`
- **TXT (Root-Domain):**
  - SPF: `v=spf1 include:_spf.google.com ~all`
  - Site-Verification: `google-site-verification=<token>` (in Google Admin Console nachschauen)
- **TXT (`google._domainkey.<domain>`):**
  - DKIM-Key (langer Wert, in Google Admin Console → Apps → Gmail → Authenticate Email)
- **TXT (`_dmarc.<domain>`):**
  - DMARC-Policy (z.B. `v=DMARC1; p=quarantine; rua=mailto:dmarc@<domain>`)

**Wichtig:** TXT-Werte ohne Anführungszeichen kopieren wenn Hetzners Eingabefeld die selbst setzt — sonst werden Anführungszeichen doppelt und der Record ist invalid.

### Forwarding-Setups (sokolar.com)

Meist nur **MX** + **SPF**:

- **MX:** ein Eintrag, je nach Forwarding-Provider (z.B. `mx.improvmx.com`, `mx1.forwardemail.net`)
- **TXT (SPF):** `v=spf1 include:<provider-spf> ~all` damit ausgehende Mails nicht in Spam landen

### Test-Tools

- **MXToolbox** ([mxtoolbox.com](https://mxtoolbox.com/)) — schnell-Check aller Mail-Records
- **Mail-Tester** ([mail-tester.com](https://www.mail-tester.com/)) — sendet Test-Mail dorthin, kriegt ausführliche Diagnose von SPF/DKIM/DMARC
- **dig** im Terminal — schnelles Records-Lookup

---

## Migration-Reihenfolge

Nicht alle gleichzeitig. Erst die unkritischen, dann die wichtigen:

1. **Domains ohne Email** (geparkt, redirect, test) — testweise migrieren, Workflow lernen
2. **Email-Forwarding-Domains** (sokolar.com) — wenn was schiefgeht, nicht business-kritisch
3. **Google-Workspace-Domains** in aufsteigender Wichtigkeit:
   - michaelsokolar.com (persönlich)
   - littlelights.studio (Geschäft) — als letzte, wenn der Workflow dreimal sitzt

Zwischen jeder Migration mindestens 24-48h warten, um sicher zu sein dass Mails noch fliessen. Im Idealfall pro Domain 1 Woche stabilen Betrieb beobachten.

---

## Status-Tracker

21 Domains insgesamt. **Alle haben aktive Mail-Konfiguration** (per `dig` verifiziert: MX + SPF überall, DKIM auf 17 von 21). Es gibt keine "kein Mail"-Gruppe — easyname richtet das Default-Mail-Setup automatisch bei jeder Registrierung ein.

**Phase-Status-Werte:** `offen` · `in Vorbereitung` · `in Arbeit` · `propagiert` · `verifiziert` · `stabil` · `abgeschlossen`

**DNS-Scan-Ergebnis (Stand 27.04.2026):**

| Mail-Provider | Anzahl | Domains |
|---|---|---|
| **easyname Mail** | 17 | alle ausser den 4 unten |
| **Google Workspace** | 4 | littlelights.studio, littlelightsstudio.at, littlelightsstudio.com, michaelsokolar.com |

**Wichtig:** easyname-Mail-Setup heisst nicht zwingend "aktiv genutzt" — easyname legt MX/SPF/DKIM Default-mässig an. Welche Domains tatsächlich Mailboxen oder Forwardings haben, klärt der easyname-Mailbox-Audit (siehe unten). Trotzdem werden alle bei Migration mit identischer Sorgfalt behandelt — die Records müssen 1:1 mit.

### Gruppe A — easyname-Mail (Test-Domains, identische Records)

Alle 17 haben identisches Mail-Schema (gleicher MX-Server, gleicher SPF-Wert, gleicher DKIM-Selector). Kann mit Template-Approach migriert werden: einmal das exakte Records-Set bei easyname dokumentieren, dann pro Domain in Hetzner replizieren.

Reihenfolge innerhalb der Gruppe: **starten mit der unkritischsten** wo du sicher bist dass keine wichtige Mail kommt. Vorschlag fettgedruckt.

| Domain | Renewal | Aktivität | Phase 1 | Phase 2 | Notes |
|---|---|---|---|---|---|
| **nocturnedomains.com** | 10.05.2027 | ungenutzt (Helena-World-Reserve) | **NS-Cutover passiert mit Transfer** | **Phase 4b in Arbeit (27.04.2026, „being processed")** | 🔄 Pilot-Transfer aktiv |
| nocturnecodex.com | 22.03.2027 | ungenutzt (Helena-World-Reserve) | **Cutover erfolgt 27.04.2026** — NS bei easyname auf Hetzner | blockiert (ICANN-60-Tage-Lock) | Phase-2-Transfer wartet auf Lock-Ablauf |
| ~~brand-film.agency~~ | 07.02.2027 | DROP — Doppelung mit brandfilm.agency | ❌ Drop | ❌ Drop | bei easyname auslaufen lassen |
| ~~brandfilm.agency~~ | 07.02.2027 | DROP — Doppelung mit brand-film.agency | ❌ Drop | ❌ Drop | bei easyname auslaufen lassen |
| ~~littlelights-studio.at~~ | 11.02.2027 | DROP — Bindestrich-Doppelung zu littlelightsstudio.at | ❌ Drop | ❌ Drop | bei easyname auslaufen lassen |
| ~~littlelights-studio.com~~ | 11.02.2027 | DROP — Bindestrich-Doppelung zu littlelightsstudio.com | ❌ Drop | ❌ Drop | bei easyname auslaufen lassen |
| littlelights.agency | 07.02.2027 | Brand-Schutz, Redirect → littlelights.studio | Zone-File generiert | offen | Standard-Cleanup |
| littlelights.at | 05.02.2027 | Brand-Schutz, Redirect → littlelights.studio | Zone-File generiert | offen | Standard-Cleanup |
| littlelights.media | 06.02.2027 | Brand-Schutz, Redirect → littlelights.studio | Zone-File generiert | offen | Standard-Cleanup |
| littlelights.productions | 07.02.2027 | Brand-Schutz, Redirect → littlelights.studio | Zone-File generiert | offen | Standard-Cleanup |
| ~~littlelights.pub~~ | 07.02.2027 | DROP — .pub als Publishing-TLD nicht intuitiv | ❌ Drop | ❌ Drop | bei easyname auslaufen lassen |
| michaelsokolar.at | 14.02.2027 | Brand-Schutz, Redirect → michaelsokolar.com | Zone-File generiert | offen | Standard-Cleanup |
| ferienwohnung-mistelbach.at | 15.09.2026 | aktive WordPress-Installation, **keine Mails** | Zone-File generiert (ohne MX/SPF/DKIM) | offen | A bleibt für WordPress; WP-Migration eigenes Projekt |
| helenaflinn-chronicles.com | 15.06.2026 | Brand-Schutz, Redirect → helenaflinn.com | Zone-File generiert | offen | Renewal nah, Phase 2 wirtschaftlich |
| helenaflinn.com | 15.06.2026 | Buch-Marke (GitHub Pages) + easyname Mail | Zone-File generiert (GitHub Pages 1:1) | offen | Renewal nah |
| sokolar.at | 14.02.2027 | Forwarding (bestätigt) | Zone-File generiert mit Cleanup | offen | Browser-Anzeige bleibt, Wildcard raus, autoconfig+autodiscover raus |
| sokolar.com | 26.02.2027 | **bestätigt aktiv** Forwarding + Subdomain-Hosting + Home-Server | Zone-File generiert (konservativ 1:1) | offen | komplexes Legacy — Subdomain-Cleanup wird separate Session |

### Gruppe B — Google Workspace (zuletzt, einzeln, mit Pause)

Alle Phase 1 mit mind. 1 Woche Beobachtungspause zwischen den Domains.

| Domain | Renewal | Mail-Setup | Phase 1 | Phase 2 | Notes |
|---|---|---|---|---|---|
| littlelightsstudio.at | 11.02.2027 | Google Workspace | Zone-File generiert (DKIM + DMARC ergänzt) | offen | erst |
| littlelightsstudio.com | 11.02.2027 | Google Workspace + viele Subdomains | Zone-File generiert (User-Triage + DKIM + DMARC) | offen | dann |
| michaelsokolar.com | 29.03.2027 | Google Workspace + GitHub Pages + MailerLite | Zone-File generiert (DKIM + DMARC ergänzt) | offen | dann |
| littlelights.studio | 19.05.2026 | Google Workspace + Microsoft 365 Spuren + Subdomain-Cluster | Zone-File generiert (DKIM + DMARC + Cross-Domain-Auth) | offen | **letzte**, höchste Kritikalität, Renewal nah → Phase 2 zeitnah denkbar |

---

## Vorbereitungs-Schritt 1: easyname-Mailbox-Audit

Bevor irgendwas migriert wird, **bei easyname pro Domain prüfen** was tatsächlich an Email-Setup läuft:

1. easyname → Domains → Edit → **Email**-Tab klicken
2. Drei Möglichkeiten pro Domain:
   - **Postfächer aktiv** → Domain hat eigene Mailboxen, sind weiter zu betreiben (= Migration mit MX-Erhalt)
   - **Forwarding aktiv** → Mails werden weitergeleitet, Forwarding-Einstellungen bleiben bei easyname, MX zeigt weiter dorthin
   - **Leer** → niemand nutzt aktiv Email, MX könnte theoretisch entfallen — aber sicherer trotzdem mitmigrieren falls jemand mal eine Bestellbestätigung an die Domain schickt

3. **Ergebnis pro Domain in der Tabelle oben in Spalte "Aktivität" eintragen** (statt `?`).

Sobald das gemacht ist, weisst du:
- Welche Domains du **gefahrlos zuerst** migrieren kannst (leere Mail-Konfig)
- Welche besondere Aufmerksamkeit brauchen (aktive Mailboxen, Custom Forwardings)

## Vorbereitungs-Schritt 2: easyname-Records-Template dokumentieren

Da alle 17 easyname-Domains identische Mail-Records haben, dokumentiere einmal das exakte Schema (z.B. von `nocturnedomains.com`):

```
TYP        NAME                                  WERT                                     PRIO  TTL
MX         @                                     mx-1.easyname.eu                         10    3600
MX         @                                     mx-2.easyname.eu                         20    3600
TXT        @                                     v=spf1 include:_spf.easyname.eu ~all     -     3600
TXT        easyname._domainkey                   v=DKIM1; k=rsa; p=<langer-Key>           -     3600
```

(Genaue Werte beim ersten Migrieren von der easyname-DNS-Zone abnehmen.)

Dann gilt: **identische Records pro Domain in Hetzner anlegen, nur DKIM-Key kann unterschiedlich sein** (separat pro Domain in easyname generiert). DKIM also pro Domain einzeln kopieren.

---

## Bemerkungen zur Reihenfolge

**Renewal-Dates beachten:** Bei Phase 2 zahlst du 1 Jahr Renewal mit. Domains mit nahem Renewal sind effizienter zu transferieren — Renewal-Gebühr fällt eh an, also faktisch ohne Aufpreis. Frühe Renewal-Termine (in nächsten 3 Monaten):
- `littlelights.studio` 19.05.2026
- `helenaflinn-chronicles.com` 15.06.2026
- `helenaflinn.com` 15.06.2026
- `ferienwohnung-mistelbach.at` 15.09.2026

**Domains die du nicht mehr brauchst:** Bei 21 Domains ist's die Gelegenheit auszumisten. Vor jeder Migration kurz fragen: brauche ich diese Domain noch? Nicht migrierte können bei easyname auslaufen lassen.

**Vorschlag fürs erste Migrations-Wochenende:**
1. easyname-Mailbox-Audit machen (Schritt 1 oben) — pro Domain 1-2 Min, ergibt klares Bild
2. Records-Template dokumentieren (Schritt 2 oben)
3. **Pilot:** `nocturnedomains.com` migrieren — vermutlich ungenutzt, gleiches easyname-Setup wie alle anderen, perfekter Workflow-Test
4. 24h beobachten, mit `dig` und `mail-tester.com` verifizieren
5. Bei Erfolg: weitere unkritische Domains in Batches durchmigrieren
6. Google-Workspace-Domains zuletzt, einzeln und mit Wartezeit

---

## Quick Reference

```bash
# Nameserver checken (sollte hetzner.de/.com sein nach Phase 1)
dig NS <domain> +short

# Komplette DNS-Antwort
dig <domain> ANY +noall +answer

# Mail-Records-Schnellcheck
dig MX <domain> +short
dig TXT <domain> +short
dig TXT _dmarc.<domain> +short
dig TXT google._domainkey.<domain> +short

# An welchen Server zeigt eine Subdomain?
dig <subdomain.domain> +short

# Welche Nameserver hat easyname momentan? (vor Migration als Referenz)
whois <domain> | grep -i 'name server'
```
