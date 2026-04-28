# Tech Stack — Little Lights Studio
**Stand: 2026-04-28**

Zentrale Übersicht aller Tools, Services und Provider. Lebende Datei, bei jeder Veränderung nachpflegen.

## Status-Legende
- ✅ **Aktiv & stabil** — läuft, kein Migrations-Bedarf
- 🔄 **In Migration** — gerade in Umstellung
- ⏳ **Geplant** — Entscheidung getroffen, Umsetzung steht aus
- 💤 **Legacy** — wird langfristig abgelöst
- ❓ **Offen** — Entscheidung noch nicht gefallen

---

## 1. Server & Hosting

| Layer | Provider | Status | Details |
|---|---|---|---|
| **Cloud-Server** | Hetzner Cloud (CPX32, Nuremberg) | ✅ | `46.224.59.56` / `2a01:4f8:1c18:e9d1::1`, Ubuntu 24.04, ~€16.80/Mo inkl. Backups |
| **Hosting-Layer** | Coolify (self-hosted, v4.0.0-beta.474) | ✅ | UI: `coolify.littlelights.studio`, GitHub-Auto-Deploy |
| **Container-Engine** | Docker (von Coolify gemanaged) | ✅ | — |
| **Reverse-Proxy / SSL** | Traefik (in Coolify integriert) | ✅ | Auto-Cert via Let's Encrypt |

→ Details: [`infrastructure.md`](infrastructure.md)

## 2. DNS

| Layer | Provider | Status | Details |
|---|---|---|---|
| **Authoritative DNS** | Hetzner DNS | 🔄 | 21 Zonen importiert. NS-Cutover läuft Domain-für-Domain. Erster Cutover (`nocturnecodex.com`) erfolgt 27.04.2026. NS-Cutover für `nocturnedomains.com` erfolgt automatisch mit dem Registrar-Transfer (siehe Phase 4b). |
| **Legacy DNS** | easyname | 💤 | Wird je Domain durch Hetzner abgelöst |

→ Details: [`domain-migration.md`](domain-migration.md), [`dns-zones/`](dns-zones/)

## 3. Domain-Registrar

| Layer | Provider | Status | Details |
|---|---|---|---|
| **Domain-Registrar** | easyname | 💤 | 21 Domains aktuell hier registriert. **Drop-Liste (5 Domains):** `brand-film.agency`, `brandfilm.agency`, `littlelights.pub`, `littlelights-studio.at`, `littlelights-studio.com` — werden bei easyname auslaufen gelassen, nicht migriert. |
| **Ziel-Registrar** | Hetzner Domains (via konsoleH) | 🔄 | **Pilot läuft:** `nocturnedomains.com` Transfer initiiert 27.04.2026, in „being processed". `nocturnecodex.com` durch ICANN-60-Tage-Lock blockiert, Transfer verschoben. Verbleibende 14 Domains nach Pilot-Abschluss. |

**Wichtig:** Hetzner hat keinen Standalone-Domain-Service à la Cloudflare/Porkbun. Domain-Registrierung ohne Webhosting läuft über das **konsoleH-Panel** unter [konsoleh.hetzner.com](https://konsoleh.hetzner.com), Produkt „Domains → Registration only". Bestellt wird via [accounts.hetzner.com](https://accounts.hetzner.com), das Panel-Login danach ist konsoleH.

**Ziel-Domain-Anzahl nach Migration: 16 Domains** (21 minus 5 Drops). Geschätzte Jahreskosten bei Hetzner: ~€411/Jahr.

## 4. Email

Pro Domain unterschiedlich. Mehrere Stacks parallel.

| Domain | Mail-Stack | Status | Details |
|---|---|---|---|
| `littlelights.studio` | Google Workspace | ✅ | Primary, alle Mitarbeiter-Adressen |
| `littlelightsstudio.com` | Google Workspace | ✅ | Domain-Alias / sekundär |
| `littlelightsstudio.at` | Google Workspace | ✅ | Domain-Alias / sekundär |
| `michaelsokolar.com` | Google Workspace + MailerLite (Newsletter) | ✅ | Persönliche Mail + Newsletter-Versand |
| `helenaflinn.com` | easyname Mailbox (Autoren-Email) | 💤 | Migration zu Forward Email geplant (Phase 4a) |
| `sokolar.com` | easyname Forwarding (13 Aliases → Gmail) | 💤 | Migration zu Forward Email geplant (Phase 4a) |
| `sokolar.at` | easyname Forwarding (4 Aliases) | 💤 | Migration zu Forward Email geplant (Phase 4a) |
| Brand-Schutz (12 Domains) | easyname Default-MX (ungenutzt) | 💤 | MX kann ohne Forwarding-Service ggf. gestrichen werden |
| `ferienwohnung-mistelbach.at` | keine Email | ✅ | Bewusst keine Mail-Records |

**Geplanter Forwarding-Provider (Phase 4a):** [Forward Email](https://forwardemail.net) Enhanced Protection Plan — **$3/Monat für unlimited Domains + unlimited Aliases**. Open Source. Inkludiert: outbound SMTP, DMARC Reporting, Email Analytics, API, 10 GB pooled Storage. Deckt alle aktuellen + zukünftigen LL-Studio-Domains ab.

**Authentication-Stack pro Domain:**
- Google-Workspace-Domains: SPF + DKIM (`google._domainkey`) + DMARC (`p=none`)
- littlelights.studio zusätzlich: Microsoft 365 Spuren (`MS=ms33161861`, `ms._domainkey`) + 3× Cross-Domain DMARC-Auth
- michaelsokolar.com zusätzlich: MailerLite-DKIM (`litesrv._domainkey`)

## 5. Source Control & CI/CD

| Layer | Provider | Status | Details |
|---|---|---|---|
| **Git-Hosting** | GitHub (`littlelightsstudio`) | ✅ | — |
| **CI/CD** | Coolify (GitHub-Webhook → Auto-Build → Deploy) | ✅ | GitHub-App `coolify-lls` (Installation-ID 127497266) |

## 6. Frontend & Code-Stack

| Stack | Wo | Status | Details |
|---|---|---|---|
| **Next.js (App Router) + Payload CMS** | littlelights.studio | ⏳ | In Phase 3 Design, Build kommt in Phase 4 |
| **Static HTML** | helenaflinn.com, michaelsokolar.com | 🔄 | Aktuell GitHub Pages, Migration zu Coolify Static-Site |
| **WordPress** | ferienwohnung-mistelbach.at | 💤 | Aktuell easyname-Webspace (PHP 8.4), Migration zu Coolify-Container geplant |
| **Sprache(n)** | Deutsch + Englisch (DE primär für DACH, EN für International) | ⏳ | Implementierung in Phase 4 |

## 7. Tooling rund ums Coding

| Tool | Zweck | Status |
|---|---|---|
| **Claude Code** | KI-Pair-Programming | ✅ |
| **VSCode** | Editor | ✅ |
| **Coolify** | Container-Deployment | ✅ |

## 7a. Internal Tools — `tools.littlelights.studio`

Eigenes Mini-Repo für team-interne Web-Tools. Live unter [tools.littlelights.studio](https://tools.littlelights.studio).

| Tool | Zweck | Status | Details |
|---|---|---|---|
| **Karrierestories Dispo Generator** | Drehpläne aus Notion-Transkripten + Claude | ✅ | `poc-dispo-generator`, API-Anbindung an Anthropic + Notion |
| **Karrierestories Crew-Kalkulator** | Berechnet Crew-Vergütung für Karrierestory- und Recruiting-Imagefilm-Produktionen, PDF-Export pro Rolle | ✅ | `poc-karrierestories-kalkulator`, basiert auf STRABAG-Rahmenvertrag 2026, PDF via Puppeteer |

**Stack:** Express + Vanilla HTML/JS (für simple Tools) + React 18 via Babel Standalone (für komplexere). Keine Build-Step, kein Webpack. Repo: [github.com/littlelightsstudio/littlelights-tools](https://github.com/littlelightsstudio/littlelights-tools). Hosting: derselbe Coolify wie die Hauptseite, Auto-Deploy via Dockerfile.

## 8. Analytics & Monitoring

| Tool | Zweck | Status | Details |
|---|---|---|---|
| **Umami** | Web-Analytics (privacy-first, kein Cookie-Banner nötig) | ⏳ | Self-hosted auf Coolify geplant |
| **Hetzner Cloud Backups** | VM-Snapshots, daily, 7 Tage Retention | ✅ | aktiv (€2.80/Mo) |
| **Coolify-DB-Backups** | App-spezifische Datenbank-Backups | ⏳ | Wird mit erstem DB-Container aktiviert |
| **Uptime Kuma** | Status-Page / Uptime-Monitoring | ❓ | Nice-to-have, nicht Priorität |

## 9. Marketing & Reach

| Tool | Zweck | Status | Details |
|---|---|---|---|
| **MailerLite** | Newsletter-Versand (michaelsokolar.com) | ✅ | DKIM via `litesrv._domainkey` |
| **Google Search Console** | SEO-Monitoring | ⏳ | Setup in Phase 6 Launch |
| **Calendly** | Booking (R&S / Workshop) | ⏳ | Wird in Phase 4 Build integriert |

## 10. Video & Media

| Tool | Zweck | Status | Hinweis |
|---|---|---|---|
| **Vimeo** | Video-Hosting (Premium-Optik) | ❓ | Eine der zwei Optionen |
| **Bunny.net** | Video-CDN (günstiger, eigener Player) | ❓ | Eine der zwei Optionen |

→ Entscheidung kommt mit Phase 4 Build.

## 11. Branding & Design-Tools

| Tool | Zweck |
|---|---|
| **Figma** | Design-Prototypen (begrenzt eingesetzt — gebaut wird im Code) |
| **Canva** | Brand-Collateral (Stream 2, ausstehend) |

---

## Per-Domain-Stack-Übersicht

Alle 21 LL-Studio-Domains, gruppiert nach Verwendung:

| Domain | Web-Stack | Email-Stack | DNS | Registrar | Status |
|---|---|---|---|---|---|
| `littlelights.studio` | Alter Webhost (188.40.29.55) → Next.js+Payload @ Coolify | Google Workspace | Hetzner DNS | easyname | DNS ready, Cutover ausstehend |
| `littlelightsstudio.com` | (Brand-Alias, Subdomains aktiv) | Google Workspace | Hetzner DNS | easyname | DNS ready, Cutover ausstehend |
| `littlelightsstudio.at` | (Brand-Alias) | Google Workspace | Hetzner DNS | easyname | DNS ready, Cutover ausstehend |
| `michaelsokolar.com` | GitHub Pages → Coolify Static | Google Workspace + MailerLite | Hetzner DNS | easyname | DNS ready, Cutover ausstehend |
| `helenaflinn.com` | GitHub Pages → Coolify Static | easyname Mailbox → Forward Email | Hetzner DNS | easyname | DNS ready, Cutover ausstehend |
| `helenaflinn-chronicles.com` | easyname HTTP-Redirect → Coolify Redirect | easyname Default | Hetzner DNS | easyname | DNS ready, Cutover ausstehend |
| `sokolar.com` | easyname Subdomains/Webspace → Triage | easyname Forwarding (13 Aliases) → Forward Email | Hetzner DNS | easyname | DNS ready (1:1), Cutover ausstehend |
| `sokolar.at` | easyname Webspace → ❓ | easyname Forwarding (4 Aliases) → Forward Email | Hetzner DNS | easyname | DNS ready, Cutover ausstehend |
| `michaelsokolar.at` | easyname HTTP-Redirect → Coolify Redirect | easyname Default | Hetzner DNS | easyname | DNS ready, Cutover ausstehend |
| `ferienwohnung-mistelbach.at` | easyname WordPress → Coolify WordPress | keine | Hetzner DNS | easyname | DNS ready, Cutover ausstehend |
| `nocturnedomains.com` | (Helena-World-Reserve) | easyname Default | **Hetzner DNS (live)** | **Hetzner Domains (Transfer in Arbeit, 27.04.2026)** | 🔄 Pilot-Transfer läuft |
| `nocturnecodex.com` | (Helena-World-Reserve) | easyname Default | **Hetzner DNS (live)** | easyname (durch ICANN-60-Tage-Lock blockiert) | ✅ DNS-Cutover 27.04.2026, Registrar-Transfer wartet auf Lock-Ablauf |
| ~~`brand-film.agency`~~ | DROP | DROP | DROP | easyname (auslaufen lassen) | ❌ Drop-Liste, nicht migrieren |
| ~~`brandfilm.agency`~~ | DROP | DROP | DROP | easyname (auslaufen lassen) | ❌ Drop-Liste, nicht migrieren |
| `littlelights.agency` | easyname HTTP-Redirect → Coolify Redirect | easyname Default | Hetzner DNS | easyname → Hetzner Domains | DNS ready, Cutover ausstehend |
| `littlelights.at` | easyname HTTP-Redirect → Coolify Redirect | easyname Default | Hetzner DNS | easyname → Hetzner Domains | DNS ready, Cutover ausstehend |
| `littlelights.media` | easyname HTTP-Redirect → Coolify Redirect | easyname Default | Hetzner DNS | easyname → Hetzner Domains | DNS ready, Cutover ausstehend |
| `littlelights.productions` | easyname HTTP-Redirect → Coolify Redirect | easyname Default | Hetzner DNS | easyname → Hetzner Domains | DNS ready, Cutover ausstehend |
| ~~`littlelights.pub`~~ | DROP | DROP | DROP | easyname (auslaufen lassen) | ❌ Drop-Liste, nicht migrieren |
| ~~`littlelights-studio.at`~~ | DROP | DROP | DROP | easyname (auslaufen lassen) | ❌ Drop-Liste, nicht migrieren |
| ~~`littlelights-studio.com`~~ | DROP | DROP | DROP | easyname (auslaufen lassen) | ❌ Drop-Liste, nicht migrieren |

---

## Zukünftige Migrationen (Reihenfolge)

1. **Phase 1 (DNS-Cutover):** Alle 21 Domains von easyname-NS auf Hetzner-NS umstellen — in Arbeit, 1/21 fertig
2. **Coolify-Apps-Setup:** helenaflinn.com → michaelsokolar.com → littlelights.studio → ferienwohnung-mistelbach.at als Coolify-Container
3. **Phase 3 (Redirect-Migration):** 12 Brand-Schutz-Domains' Redirects von easyname auf Coolify Traefik
4. **Phase 4a (Email-Migration):** sokolar.com + sokolar.at + helenaflinn.com Email zu Forward Email
5. **Phase 4b (Registrar-Transfer):** Domain-für-Domain easyname → Hetzner Domains (via konsoleH). **Pilot: `nocturnedomains.com` (Transfer initiiert 27.04.2026, in Bearbeitung).** `nocturnecodex.com` durch ICANN-60-Tage-Lock blockiert, Transfer nachgezogen sobald Lock abläuft.
6. **Phase 5 (easyname-Cancellation):** Webhosting + Email-Account bei easyname kündigen, sobald alle Domains migriert

---

## Provider-Übersicht & Kosten (Monatsschätzung)

| Provider | Was | Kosten |
|---|---|---|
| Hetzner Cloud (Server + Backups) | Production-Server | ~€16.80 |
| Hetzner DNS | DNS-Hosting für 16 Zonen (nach Drops) | gratis |
| Hetzner Domains (via konsoleH) | Registrar für 16 Domains | ~€411/Jahr (= ~€34/Mo) — siehe Domain-Migration-Doku für Detail-Breakdown |
| Google Workspace | Mail für 4 Domains | ~€6/User/Mo (Business Starter) |
| Forward Email | Mail-Forwarding für **unlimited Domains** (alle LL-Studio mit Forwarding-Bedarf) | $3 (~€2.80) |
| MailerLite | Newsletter | abhängig von Subscriber-Count |
| GitHub | Source Control | gratis (für public repos) |
| Vimeo / Bunny.net | Video-Hosting | TBD nach Entscheidung |

**Total laufende Infrastruktur (geschätzt): ~€20-25/Monat** (ohne Workspace und Marketing-Tools, die separat budgetiert sind).

---

## Updates an dieser Datei

Bei jeder Statusänderung hier nachpflegen. Insbesondere:
- Phase 1 Cutover je Domain → Status-Spalte updaten
- Wenn Coolify-App live geht → Web-Stack-Spalte updaten
- Bei Email-Migration → Email-Stack-Spalte updaten
- Bei Registrar-Transfer → Registrar-Spalte updaten

Diese Datei ist die zentrale "wo stehen wir mit der Tech"-Übersicht. Detail-Docs:
- [`infrastructure.md`](infrastructure.md) — Server-Konfiguration im Detail
- [`domain-migration.md`](domain-migration.md) — DNS-Migrations-Plan + Status-Tracker
- [`dns-zones/README.md`](dns-zones/README.md) — Zone-File-Konventionen
- [`dns-zones/triage.md`](dns-zones/triage.md) — User-Entscheidungen pro Sonderfall
- [`roadmap.md`](roadmap.md) — Stream 4 Infrastruktur (high-level Roadmap)
