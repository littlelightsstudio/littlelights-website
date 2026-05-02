% DNS-Zone-Triage — offene Entscheidungen vor Bulk-Generation

**Workflow:** Du beantwortest jeweils unter "**Antwort:**" mit `>`-Prefix. Ich lese das File danach in einem Schwung und generiere alle Zone-Files entsprechend.

**Default-Konvention** (gilt überall sofern nicht anders entschieden):
- ENTFERNT: `*` Wildcard, `autoconfig`, `autodiscover`, `ftp`, `mail`, `webmail`
- BEHALTEN: A root, A www, MX (×2), SPF TXT, `easyname._domainkey` CNAME, AAAA wenn vorhanden
- Bei Google-Workspace 1:1 übernehmen, kein Cleanup

---

## A) Bulk-Gruppe — 12 Standard-easyname-Domains

Identisches DNS-Schema, Subdomain-Tab zeigt nur "Referral" oder "Parked notice", keine Speziallinks. Ich würde alle 12 mit dem Standard-Cleanup-Pattern bauen. Pro Domain ist nichts Eigenes zu entscheiden — eine Sammelfrage:

- brand-film.agency
- brandfilm.agency
- helenaflinn-chronicles.com
- littlelights-studio.at
- littlelights-studio.com
- littlelights.agency
- littlelights.at
- littlelights.media
- littlelights.productions
- littlelights.pub
- michaelsokolar.at
- nocturnecodex.com

**Frage A.1:** Standard-Cleanup-Pattern (Wildcard + autoconfig + autodiscover raus, A root + A www + AAAA + MX + SPF + DKIM-CNAME bleiben) für alle 12 ok?

**Antwort:**
> ja das passt für alle 12. das sind nur brand defence domains die alle auf die haupt-domain weiterleiten

**Frage A.2:** Bei allen 12 sind die HTTP-Redirects (z.B. `brand-film.agency` → `http://www.brand-film.agency/...`) im easyname-Subdomains-Tab konfiguriert, NICHT in DNS. Solange A-Records auf `77.244.243.53` zeigen, laufen die Redirects weiter. Bestätigung: redirects bleiben in easyname stehen, ich migriere nur DNS, Redirects passieren weiter über easyname's Hosting-Layer. OK?

**Antwort:**
> die redirets bleiben vorerst bei easyname

---

## B) ferienwohnung-mistelbach.at — WordPress-Verdacht

Subdomain-Tab zeigt: **Root = "Web space content PHP 8.4"** (= aktive PHP/WordPress-Installation auf easyname-Webspace). www = "Referral".

DNS-Records (easyname-Standard, kein AAAA):
```
@   A     77.244.243.53
*   A     77.244.243.53   ← raus
www A     77.244.243.53
@   MX 10 mx01/mx02.easyname.eu
@   TXT   v=spf1 include:spf.easyname.com -all
easyname._domainkey  CNAME  dkim.easyname.com
autoconfig/autodiscover CNAME mailconfig.easyname.com  ← raus
```

**Frage B.1:** Ist das die WordPress-Installation aus dem Roadmap-Sonderfall? (Du erwähntest im README, dass eine Domain WordPress hostet.)

**Antwort:**
> genau, das ist die wordpress installation die noch heikel ist. wordpress migration ist ein separates projekt dass wir gesondert angehen.

**Frage B.2:** Falls ja → A bleibt auf `77.244.243.53`, WordPress läuft unverändert weiter. WordPress-Migration (Files + DB) ist separates Projekt. OK so?

**Antwort:**
> ok so

**Frage B.3:** Gibt's hier Mail-Forwarding (z.B. info@ferienwohnung-mistelbach.at → privates Postfach), oder ist Mail nur der easyname-Default? Falls kein Forwarding aktiv → MX könnte theoretisch raus, ich würd's trotzdem behalten als Sicherheitsnetz. OK?

**Antwort:**
> nein, hierfür gibt es keine emails

---

## C) helenaflinn.com — GitHub Pages + easyname Mail

Spannender Sonderfall. Kein Subdomain-Tab-Screenshot dabei.

DNS-Records:
```
@   A     185.199.108.153   (GitHub Pages)
@   A     185.199.109.153   (GitHub Pages)
@   A     185.199.110.153   (GitHub Pages)
@   A     185.199.111.153   (GitHub Pages)
www CNAME littlelightsstudio.github.io.
@   MX 10 mx01/mx02.easyname.eu
@   TXT   v=spf1 include:spf.easyname.com -all
easyname._domainkey  CNAME  dkim.easyname.com
autoconfig/autodiscover CNAME mailconfig.easyname.com  ← raus
```

**Frage C.1:** Records 1:1 übernehmen mit Standard-Cleanup (autoconfig/autodiscover raus, kein Wildcard vorhanden), inkl. GitHub-Pages-A-Records und CNAME für www? Bestätigung dass Buch-Marke noch via GitHub Pages läuft.

**Antwort:**
> ja das läuft aktuell alles über github, werden wir irgendwann mal migrieren auf hetzner, aber belassen wir jetzt genau so wie es ist

**Frage C.2:** Hast du einen Subdomain-Tab-Screenshot von helenaflinn.com vergessen, oder ist da nichts konfiguriert? (Bei den anderen Domains gibts den, hier fehlt er.)

**Antwort:**
> im subdomain tab ist nichts enthalten

**Frage C.3:** Mail-Forwarding aktiv? (Mail-Tab nicht im Screenshot enthalten.)

**Antwort:**
> kein mail forwarding, läuft alles über meine autoren email

---

## D) michaelsokolar.com — Google + GitHub + MailerLite

DNS-Records:
```
@   MX 1   SMTP.GOOGLE.COM           (Google Workspace, neuer 1-MX-Stil)
@   TXT   google-site-verification=fKNdo9iA6z1GpJOL7tqt5IZ2ZlCsEDho...
@   TXT   v=spf1 include:_spf.mlsend.com include:_spf.google.com ~all
@   A     185.199.108.153            (GitHub Pages)
@   A     185.199.109.153
@   A     185.199.110.153
@   A     185.199.111.153
litesrv._domainkey CNAME litesrv._domainkey.mlsend.com.
www CNAME littlelightsstudio.github.io.
```

Kein Wildcard, kein autoconfig/autodiscover, kein easyname-DKIM — clean. Kein Subdomain-Tab-Screenshot dabei.

**Frage D.1:** Records 1:1 übernehmen (Google MX + GitHub Pages + MailerLite-DKIM + alle TXT)? Standard für moderne Setups.

**Antwort:**
> ja genau, 1:1 übernehmen

**Frage D.2:** Subdomain-Tab vergessen oder leer?

**Antwort:**
> kein subdomain tab

**Frage D.3:** Sehe **keinen Google-Workspace-DKIM-Record** (`google._domainkey.michaelsokolar.com` CNAME oder TXT). Ist das Absicht (DKIM in Google Admin Console nicht eingerichtet) oder fehlt's einfach im Screenshot? Ohne DKIM landen ausgehende Gmails öfter im Spam — beim Migrieren wäre Gelegenheit, das nachzurüsten.

**Antwort:**
> keine ahnung warum, aber die domain läuft über google business 

---

## E) littlelights.studio — Geschäftskritisch, viele Spuren

Größte und kritischste Zone. DNS-Records:

```
@   MX 1    smtp.google.com           (Google Workspace)
@   TXT    MS=ms33161861              (Microsoft 365 verification)
@   TXT    google-site-verification=SYQ7CN49MLzewVuAGgERHnH7CUATxKei...
@   TXT    google-site-verification=pZ2oF9aqDNaSLHDA10CBUHJKMb3WYvQQ...
@   TXT    v=spf1 include:_spf.google.com ~all
ms_._domainkey TXT k=rsa; p=MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQCaR1AGYi0G...   (Microsoft DKIM)

@   A      188.40.29.55               (??? — wo ist das?)
*   A      77.244.243.53              (Wildcard auf easyname)

backup       A     81.223.179.78      (Home-Server)
gcal         CNAME ghs.googlehosted.com.
gdrive       CNAME ghs.googlehosted.com.
groups       CNAME ghs.googlehosted.com.
mail         CNAME ghs.googlehosted.com.
media        A     77.244.243.53      (easyname Webspace, "Web space content PHP 8.4")
publishing   AAAA  2a01:aee0:0:6::11
publishing   A     77.244.243.53      (easyname Webspace, "Hidden referral")
studio       A     81.223.179.78      (Home-Server)
surveillance A     81.223.179.78      (Home-Server)
tools        AAAA  2a01:4f8:1c18:e9d1::1
tools        A     46.224.59.56       (Hetzner Coolify Production)
vpn          A     81.223.179.78      (Home-Server)
www          A     188.40.29.55       (gleiche IP wie root)
```

**Frage E.1:** **`@` und `www` zeigen auf `188.40.29.55`**. Das ist Hetzner Online (anderer Block als `46.224.59.56`). Wo läuft die Website aktuell? Ich vermutete sie liefe auf `46.224.59.56` (Coolify). Aktueller Stand?

**Antwort:**
> die website läuft aktuell über meinen alten webseiten host. das belassen wir so lange bis die seite neu gebaut ist von uns

**Frage E.2:** **Microsoft 365** (`MS=ms33161861` + `ms_._domainkey`) — wird das noch genutzt? Falls nicht: rauswerfen, Records sind dann verwaist und unnötig. Oder behalten für die Zukunft?

**Antwort:**
> ich hab keine ahnung, lassen wir es mal lieber so

**Frage E.3:** **Wildcard `*` → 77.244.243.53** — willst du den behalten? Default wäre raus (alle echten Subdomains sind explizit definiert). Falls eine versteckte easyname-Forwarding-Regel existiert die einen unbekannten Subdomain braucht, müsste der Wildcard bleiben.

**Antwort:**
> es braucht keine wildcard

**Frage E.4:** **Subdomains auf Home-Server `81.223.179.78`** (backup, studio, surveillance, vpn) — alle aktiv? Welche kann raus?

**Antwort:**
> die belassen wir mal so

**Frage E.5:** **easyname-Subdomains** (media → "Web space content PHP 8.4", publishing → "Hidden referral") — beide aktiv genutzt, oder welche raus? Was läuft konkret unter media.littlelights.studio?

**Antwort:**
> media belassen wir mal so bis die neue webseite steht

**Frage E.6:** **Google CNAMEs** (gcal, gdrive, groups, mail → ghs.googlehosted.com) — sind das alte Google-Sites/Short-URLs aus Workspace-Admin? Aktiv genutzt oder Karteileichen?

**Antwort:**
> ich bin mir nicht sicher, lassen wir sie lieber mal

**Frage E.7:** **`tools.littlelights.studio` auf Hetzner Coolify (46.224.59.56)** — bleibt klar. AAAA `2a01:4f8:1c18:e9d1::1` auch behalten, ja?

**Antwort:**
> ja belassen

**Frage E.8:** Kein **Google DKIM** (`google._domainkey`) in den Records sichtbar. Bei dieser Geschäftsdomain wäre das ein Muss — beim Cutover gleich nachrüsten? Du müsstest dafür den DKIM-Key aus Google Admin Console (Apps → Gmail → Authenticate Email) holen, ich trag ihn dann ein.

**Antwort:**
> das ist sehr komisch - ich versteh es selbst nicht. hier der dkim. kann man den auch für michaelsokolar.com nutzen?
DNS host name (TXT record name):
google._domainkey
TXT record value:
v=DKIM1; k=rsa; p=MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEA4GWzBwvEhTH0JsQKiyq5UYwd9xI1+oRLiA2actNNCQ91zOypyiZN83nBEhTJx1sEkHPEaAzZP4t5eEyZxMolj2NrOaXfgeAGhog52f2Xfp6Kzj6TlKAtb5PFm2ntpd3BUUlv1vMkii7kF0Z/tyESOsMW6v8AFQUj60YPtOrdSSysNumGPt1iOn0QvHptSzlRM3smciozD/3FZ9mFW8JdjwsUQaBehBsBQ0GtJM6EY67l7rnUfF22fS34SliDDLyLu0Ai4+BRP+tWbfzlPPz0lk6HYmEBzpo175Jgf+anldVWUC7Apy4+Hpg0TzlfNe1uTcALFO1XJNAvSlFMVnwH7QIDAQAB

**Frage E.9:** **DMARC-Record** (`_dmarc.littlelights.studio` TXT) ist auch nicht im Screenshot sichtbar. Existiert nicht oder fehlt im Screenshot? Falls nicht existent: gleich mit anlegen (z.B. `v=DMARC1; p=none; rua=mailto:dmarc@littlelights.studio`)?

**Antwort:**
> ja bitte mit anlegen, was auch immer das ist

---

## F) littlelightsstudio.com — Google + viele easyname-Webspace-Subdomains

DNS-Records:
```
@   MX 1   SMTP.GOOGLE.COM
@   TXT    google-site-verification=hAM4NSsw50lTVATSMZWe56sv8aHcGMjQ...
@   TXT    v=spf1 include:_spf.google.com ~all
@   A      77.244.243.53
*   A      77.244.243.53      (Wildcard)

backup       A 81.223.179.78
branded      A 77.244.243.53   (Web space content PHP 8.4)
cloud        A 77.244.243.53
dev          A 77.244.243.53   (Web space content PHP 8.4)
married      A 77.244.243.53   (Web space content PHP 8.4)
media        A 77.244.243.53   (Web space content PHP 8.4)
sandbox      A 77.244.243.53   (Web space content PHP 8.4)
studio       A 81.223.179.78
surveillance A 81.223.179.78
www          A 77.244.243.53   (Referral → http://littlelights.studio/)
```

Subdomain-Tab zeigt zusätzlich:
- root → "Referral" zu `https://www.littlelightsstudio...`
- cloud → "Referral" zu `http://studio.littlelights....`

**Frage F.1:** **Wildcard raus?** (Default-Empfehlung: ja, alle echten Subdomains sind explizit.)

**Antwort:**
> wildcard raus. zusätzliche folgendes raus: branded, cloud, married, sandbox

**Frage F.2:** Welche der **PHP-Webspace-Subdomains** sind noch aktiv?
- `branded` — was läuft da?
- `dev` — Sandbox/Dev-Umgebung?
- `married` — Hochzeitsseite?
- `media` — Medien?
- `sandbox` — Test?

Bitte einzeln markieren: bleibt / raus.

**Antwort:**
> branded: raus
> dev: belassen
> married: raus
> media: belassen
> sandbox: raus

**Frage F.3:** **Home-Server-Subdomains** (backup, studio, surveillance auf 81.223.179.78) — bleiben oder raus?

**Antwort:**
> backup: belassen
> studio: belassen
> surveillance: belassen

**Frage F.4:** **`cloud.littlelightsstudio.com`** ist Subdomain-Redirect → `http://studio.littlelights....`. Bleibt? (Wenn ja, A-Record bleibt auf 77.244.243.53 damit Redirect funktioniert.)

**Antwort:**
> raus damit

**Frage F.5:** Google DKIM + DMARC siehe E.8/E.9 — gleiche Frage hier.

**Antwort:**
> siehe oben - können wir das mit verwenden?

---

## G) littlelightsstudio.at — Google Workspace, schlank

DNS-Records (kein Subdomain-Tab-Screenshot dabei):
```
@   MX 1   smtp.google.com
@   TXT    google-site-verification=WLLcabbxKJTk_YcqL2KC00AFDxi8KOWp...
@   TXT    v=spf1 include:_spf.google.com ~all
@   A      77.244.243.53
*   A      77.244.243.53      (Wildcard)
www A      77.244.243.53
```

**Frage G.1:** Records 1:1 + Standard-Cleanup (Wildcard raus)? Bleibt nur A root, A www, Google MX/SPF/Verification.

**Antwort:**
> standard cleanup

**Frage G.2:** Subdomain-Tab Screenshot vergessen oder leer?

**Antwort:**
> leer

---

## H) sokolar.com — komplexes Legacy

Im README schon als Triage-Fall markiert. Vorschlag: **separate Session danach**, nicht in diesem Schwung. Hier nur die Vorab-Frage:

**Frage H.1:** OK, sokolar.com nehmen wir als allerletztes nach allen anderen 18 Domains? Dann läuft Bulk-Aufbau nicht in die komplexe Triage rein.

**Antwort:**
> 

---

## I) Fehlende Email-Tab-Screenshots

Du hast nur für sokolar.at und sokolar.com den Email-Tab geschickt. Für die anderen 19 fehlt er.

**Frage I.1:** Per Default behandle ich alle als "easyname-Default-Mail-Setup, MX bleibt". Bestätigung dass keine der 19 Domains aktive Forwarding-Aliases hat von denen ich wissen müsste? (Falls doch eine: Domain nennen, ich pass an.)

**Antwort:**
> alle wo ich keinen screenshot hinterlegt habe, haben kein fowarding

---

## J) Reihenfolge des Bulk-Aufbaus

**Frage J.1:** Reihenfolge nach Risiko (von niedrig nach hoch):

1. Gruppe A — die 12 Standard-Bulk-Domains (Brand-Schutz, kein Aktivverkehr)
2. ferienwohnung-mistelbach.at (WordPress-Schutz)
3. helenaflinn.com (GitHub Pages, einfach)
4. littlelightsstudio.at (Google Workspace, schlank)
5. michaelsokolar.com (Google + GitHub + MailerLite)
6. littlelightsstudio.com (Google + viele Subdomains)
7. littlelights.studio (geschäftskritisch, max. Komplexität)
8. sokolar.com (separate Session)

OK so?

**Antwort:**
> ja passt. ich würde aber gerne jetzt schon mal alle zone files anlegen

---

## K) Sonstiges / freie Notes

Falls du beim Durchgehen noch was bemerkst (vergessene Subdomain, Hinweis aus deiner Erinnerung, etc.):

**Antwort:**
> 

---

## L) Vermerk: Phase 3 — easyname-Redirects auf Coolify migrieren

**Nicht jetzt — eigenes Projekt nach DNS+Registrar-Migration.** Hier nur dokumentiert damit's nicht vergessen geht.

**Hintergrund:** DNS macht keine HTTP-Redirects. Aktuell laufen die Subdomain-Weiterleitungen (z.B. `brand-film.agency` → `littlelights.studio`) über easyname's Webserver auf `77.244.243.53`. Solange die A-Records dort hin zeigen, funktionieren die Redirects auch nach Phase 1+2 weiter.

**Ziel:** easyname langfristig komplett ablösen. Voraussetzung: Redirects müssen woanders laufen.

**Lösung:** **Coolify Reverse-Proxy (Traefik)** auf Hetzner-Server `46.224.59.56`. Pro Brand-Schutz-Domain eine Redirect-Regel.

**Migrations-Pfad:**
1. Coolify-Redirect-Konfig anlegen (Traefik- oder Caddy-Routes mit 301 zur Ziel-URL)
2. Pro Domain: A-Record bei Hetzner DNS von `77.244.243.53` (easyname) → `46.224.59.56` (Coolify) umstellen
3. Verifizieren: Aufruf `brand-film.agency` → 301 → `littlelights.studio`
4. Wenn alle Domains umgezogen sind: easyname-Webhosting kündigen

**Skaliert für** alle 12 Bulk-Brand-Schutz-Domains + ggf. helenaflinn-chronicles.com.

**Sonderfall ferienwohnung-mistelbach.at:** WordPress-Migration (Files + DB) ist eigenes Projekt — getrennt von der Redirect-Migration.

**→ Wird in [`roadmap.md`](../roadmap.md) unter "Infrastruktur & Hosting" getrackt.**
