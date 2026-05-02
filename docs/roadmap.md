# Little Lights Studio — Rebranding Roadmap
**Letzte Aktualisierung: 2. Mai 2026**

---

## Projektübersicht

Dieses Projekt ist mehr als eine Website — es ist ein **komplettes Rebranding** von Little Lights Studio. Die Website ist der erste und wichtigste Baustein, auf dem alles Weitere aufbaut.

| Stream | Status | Beschreibung |
|--------|--------|-------------|
| **Stream 1: Website** | 🔄 In Arbeit | Analyse → Strategie → Design → Build → Launch |
| **Stream 2: Brand Collateral** | ⏳ Ausstehend | Office-Vorlagen, Visitenkarten, Präsentationen |
| **Stream 3: Brand Guidelines** | ⏳ Ausstehend | Styleguide, Nutzungsregeln, Asset-Library |
| **Stream 4: Infrastruktur & Hosting** | 🔄 In Arbeit | Server, DNS, Domain-Migration, Legacy-Ablösung |

---

## Stream 1: Website

### Phase 1: Analyse ✅
**Abgeschlossen: 7. April 2026**

| Dokument | Status |
|----------|--------|
| [1.1 Aktuelle Website analysieren](phase1/1.1_aktuelle_website_analyse.md) | ✅ |
| [1.2 Konkurrenzanalyse](phase1/1.2_konkurrenzanalyse.md) | ✅ |
| [1.3 Positionierung](phase1/1.3_positionierung.md) | ✅ |
| [1.4 SEO-Analyse & Keyword-Strategie](phase1/1.4_seo_analyse.md) | ✅ |
| [1.5 Reels & Stories Wettbewerbsanalyse](phase1/1.5_reels_stories_wettbewerb.md) | ✅ |

Kernerkenntnisse:
- EB-Marktführerschaft als zentraler Differenziator (150+ Karrierestories)
- Strategische Partnerschaft als Geschäftsmodell (nicht nur Claim)
- Storytelling-Beweise statt Claims (Agency + Reels + Fantasy-Trilogie)
- Feld "Strategischer Partner" komplett frei bei der Konkurrenz
- Little Lights rankt für keinen relevanten Begriff in den Top 10

### Phase 2: Strategie & Konzept ✅
**Abgeschlossen: 12. April 2026**

| Dokument | Status |
|----------|--------|
| [2.1 Messaging-Architektur](phase2/2.1_messaging_architektur.md) | ✅ |
| [2.2 Homepage-Dramaturgie](phase2/2.2_homepage_dramaturgie.md) | ✅ |
| [2.3 Seitenarchitektur](phase2/2.3_seitenarchitektur.md) | ✅ |
| [2.4 SEO-Strategie](phase2/2.4_seo_strategie.md) | ✅ |

Kernerkenntnisse:
- 5-Sektionen-Journey: Hero → Bereiche → Beweis → Partnerschaft → CTA
- Finale Seitenstruktur mit allen URLs und internem Linking
- Brand Statement, Tonalitätsregeln, Messaging pro Bereich
- GEO-Strategie für AI-Suche definiert

### Phase 3: Design 🔄
**Start: 12. April 2026**

| Dokument | Status |
|----------|--------|
| [3.1 Design Inspiration](phase3/3.1_design_inspiration.md) | ✅ |
| [3.1 Design Status](phase3/3.1_design_status.md) | ✅ Gelockt |
| [3.2 Tech Stack](phase3/3.2_tech_stack.md) | ✅ |
| [3.3 Design Tasks](phase3/3.3_design_tasks.md) | 🔄 In Arbeit |

Gelockt:
- Farbpalette: Navy #0f1b2d + Warm Cream #F7F6F3 + Copper #C8956C
- Typografie: Clash Display (Headings) + Satoshi (Body), negative Tracking bei Headlines
- Designsprache: Hell als Basis, dunkle Sektionen für Rhythmus, Diagonale als Leitmotiv
- Homepage MVP: 8 Sektionen mit Sticky Stacking, Footer-Reveal, Lenis + GSAP
- Three-Split Slider: Diagonale Clips, Copper Divider, Hover-Expansion
- Methode: Isoliert bauen → testen → integrieren

**Bereits gebaut (Stand Session 7, 02.05.2026):**
- Hero-Variants: `full` (Homepage, animiert), `landing` (Disziplin-Hubs mit Foto + Triangle), `editorial` (Pages ohne Foto, mit/ohne Triangle), `reduced`
- Block-Library für Pages.sections: `hero`, `bold-statement`, `text-section` (RichText), `magazine-manifest` (Editorial-Fließtext mit Drop-Cap + Pull-Quote), `team-grid` (4-Col mit Hover-Crossfade), `diagonal-slider`, `projects-grid`, `stats`, `cta`, `testimonials`, `client-logos`
- Globals: `Header` (Mega-Menu) + `Footer` (5 Spalten mit auto-from-parent + manual-Modi) + `SiteSettings`
- Wiederverwendbares `FooterReveal`-Pattern für alle dynamischen Pages
- Erste komplette Sub-Page: **Über Uns** (Hero editorial + Bold + Magazine Manifest + Team Grid)
- Legal-Pages-Infrastruktur: TextSection mit Lese-Typografie (h2/h3, Listen, Links, Blockquotes)

Nächste Schritte → siehe [3.3 Design Tasks](phase3/3.3_design_tasks.md). Operativ:
- TeamMembers in Payload befüllen (Photos + Hover-Photos + Socials)
- Legal-Pages anlegen + Inhalte einsetzen (Drafts liegen vor: Impressum, Datenschutz, AGB)
- Disziplin-Pages bauen (Drei-Akt-Schema WAS/WIE/WER mit Magazine-Manifest)
- Mobile-Verifikation aller neuen Patterns

### Phase 4: Build
**🔄 In Arbeit — parallel zu Phase 3 Design**

Bereits abgeschlossen:
- ✅ Payload CMS Setup + Content-Types (Pages, Projects, Testimonials, TeamMembers, Media, MediaTags, Users) + Globals (Header, Footer, SiteSettings)
- ✅ Next.js 15 Frontend-Skeleton (`littlelights-build` Repo)
- ✅ CMS-Integration der meisten Components (siehe Phase 3 Block-Library)
- ✅ Video-Integration Bunny.net (Hero-Background-Video)
- ✅ Live-Preview-URLs für Pages und Projects (mit nested-URL-Resolver)

Noch ausstehend:
- [ ] **Zweisprachigkeit DE/EN** — Localized-Felder sind im Schema vorbereitet, aber Routing/Switcher noch nicht gebaut
- [ ] **Kontaktformular + Calendly** (nur R&S/Workshop)
- [ ] **SEO-Implementierung** — SEO-Plugin ist installiert, aber Schema Markup, Sitemap, hreflang, 301-Redirects fehlen
- [ ] **GEO-Optimierung** für AI-Suche
- [ ] **Self-Hosting der Schriften** (Satoshi, Clash Display) statt Fontshare-CDN — DSGVO-Vereinfachung (kein externer Verarbeiter), Performance-Gewinn, via `next/font/local` einbinden. Aktuell läuft via api.fontshare.com, ist im Datenschutz erwähnt
- [ ] **Markdown-Auto-Conversion im Lexical-Editor** (`MarkdownTransformersFeature`) — komfortabel für künftige Content-Edits, aktuell muss manuell im Editor formatiert werden

### Phase 5: Content
**🔄 Teilweise in Arbeit — parallel zu Build**

Bereits abgeschlossen:
- ✅ **Über Uns** Texte (Bold Statement, Magazine Manifest, Team Grid)
- ✅ **Legal-Drafts** (Impressum, Datenschutz, AGB) — paste-ready, Anwalt-Review noch offen
- ✅ **Projektdatenbank**: 39 Projekte importiert (Session 5)

Noch ausstehend:
- [ ] **Finaler Copytext** für Disziplin-Seiten (Agency, R&S, Creative Studio) auf Basis der Messaging-Architektur
- [ ] **5 Full Case Studies** einpflegen (aktuell: Helena Flinn Chronicles + I am Progress angelegt)
- [ ] **10-15 Minimal-Ansicht Projekte**
- [ ] **Testimonials einholen** und einpflegen (Block fertig seit Session 3, Filter `filterByArea` + `onlyFeatured` gebaut)
- [ ] **Team-Fotos** (Default + Hover-Variante) + Bios + Socials in CMS
- [ ] Bildmaterial und Video-Embeds
- [ ] Kundenlogos (SVG, farblich angepasst)

### Phase 6: Launch
**Ausstehend**

- 301-Redirects von alter Website
- Google Search Console einrichten
- Performance-Check (Lighthouse 90+)
- Finale QA (alle Seiten, alle Sprachen, alle Devices)
- DNS-Umzug

---

## Stream 2: Brand Collateral
**Ausstehend — nach Website-Launch**

Aufbauend auf dem Design-System der Website:

> **Tool-Option:** Claude Design (Anthropic Labs, Research Preview auf Pro/Max/Team) könnte hier stark sein — liest Design-System ein, produziert konsistente Slides/Pitch-Decks/Social-Templates/Landing-Pages, Export zu Canva/PDF/PPTX. Evaluieren wenn Website-Stream fertig.


- [ ] Office-Vorlagen (Word, PowerPoint, Google Docs/Slides)
- [ ] Visitenkarten
- [ ] E-Mail Signatur
- [ ] Angebots-/Rechnungsvorlage
- [ ] Social Media Templates (LinkedIn, Instagram)
- [ ] Präsentationsvorlage (Pitch Deck)

---

## Stream 3: Brand Guidelines
**Ausstehend — nach Website-Launch**

- [ ] Styleguide-Dokument (Farben, Typo, Bildsprache, Tonalität)
- [ ] Logo-Nutzungsregeln
- [ ] Asset-Library (Logos, Icons, Fonts, Templates)
- [ ] Do's & Don'ts

---

## Stream 4: Infrastruktur & Hosting
**Laufend — operative Spur parallel zu den Rebranding-Streams**

**Übersicht:** [`tech-stack.md`](tech-stack.md) — zentrale Karte aller Tools, Provider und Status pro Domain.

Detail-Docs: [`infrastructure.md`](infrastructure.md) (Server), [`domain-migration.md`](domain-migration.md) (DNS-Migration).

### Server (✅ steht)
- ✅ Hetzner Cloud CPX32 `lls-prod-01` (`46.224.59.56`), Ubuntu 24.04
- ✅ Coolify als Hosting-Layer, Auto-Deploy aus GitHub
- [ ] `coolify.littlelights.studio` Subdomain einrichten (aktuell nur IP:8000)

### DNS-Migration easyname → Hetzner DNS (🔄 in Arbeit, Großteil durch)
21 Domains. Strategie: erst alle Hetzner-Zonen aufbauen + verifizieren, dann kontrollierter Cutover Domain-für-Domain.

**Stand 02.05.2026 — abgeschlossen:**
- ✅ Pilot `nocturnedomains.com` + `nocturnecodex.com` (Cutover 27.04.)
- ✅ Cleanup-Konventionen etabliert ([`dns-zones/README.md`](dns-zones/README.md))
- ✅ Triage-Runde abgeschlossen ([`dns-zones/triage.md`](dns-zones/triage.md))
- ✅ DKIM-Werte für alle 4 Google-Workspace-Domains gesammelt
- ✅ Alle 21 Zone-Files generiert (Cleanup, DKIM, DMARC, Cross-Domain-Auth)
- ✅ Alle 21 Zonen in Hetzner DNS importiert
- ✅ **Pilot-Cutover littlelights.studio** mit Mail-Smoke-Test + DKIM Start Authentication in Google Admin
- ✅ **4 Brand-Schutz-Domains NS umgezogen:** littlelights.agency, littlelights.at, littlelights.media, littlelights.productions
- ✅ **michaelsokolar.at** NS umgezogen (Brand-Schutz-Redirect)
- ✅ **helenaflinn-chronicles.com** NS umgezogen (Brand-Schutz-Redirect)
- ✅ **ferienwohnung-mistelbach.at** NS umgezogen + Coolify-App live (Express-Server, replaced WordPress)
- ✅ **michaelsokolar.com** NS umgezogen + Coolify-App live (Static Site nginx:alpine, GitHub Pages → Coolify) + Mail-Smoke-Test + DKIM
- ✅ **Workspace-Domains littlelightsstudio.com** NS umgezogen + Mail-Smoke-Test + DKIM
- 🔄 **littlelightsstudio.at** NS gesetzt, Propagation hinkt (NIC.AT registry-langsam) — Mail-Smoke + DKIM nach Propagation

**Noch ausstehend:**
- [ ] **helenaflinn.com** — wartet auf Promotion-Ende. Nach Promotion: Hetzner-Zone-Update (GitHub-Pages-IPs → Coolify), NS-Switch, Mail-Smoke
- [ ] **sokolar.at + sokolar.com** — separate Session (Mail-Forwarding-Setup ist komplex, anderer easyname-Account, sokolar.com hat Legacy-Subdomains)

**Drops (NICHT migriert, laufen bei easyname aus):** brand-film.agency, brandfilm.agency, littlelights.pub, littlelights-studio.at, littlelights-studio.com — strategisch nicht mehr relevant, kein Renewal/Transfer.

### Registrar-Transfer easyname → Hetzner (🔄 in Arbeit)
- ✅ **littlelights.studio** Auth-Code geholt + Transfer bei Hetzner konsoleH eingereicht (mit 3 Hetzner-NS in Advanced Options, nahtloser DNS-Transfer). Wartet auf ICANN-Bestätigungsmail + Tucows→Hetzner-Handoff (~5-7 Tage)
- 🤖 Cloud-Agent geplant für 2026-05-03 15:00 CEST: Transfer-Status-Check + .at-Propagation + DKIM-Records ([Routine](https://claude.ai/code/routines/trig_01NRDn4BTEvCh8hndBoAeeBz))
- [ ] **7 weitere fertig migrierte Domains**: 4× brand-domains + michaelsokolar.at + michaelsokolar.com + helenaflinn-chronicles.com + ferienwohnung-mistelbach.at — Auth-Code holen + Transfer-Lock entfernen + via konsoleH einreichen
- [ ] **Workspace-Domains-Transfer** (littlelightsstudio.at, .com, michaelsokolar.com hat schon Transfer eingereicht — siehe oben) — beide bezahlt bis Februar 2027 bei easyname, Transfer optional bis dahin

### ~~WordPress-Migration ferienwohnung-mistelbach.at~~ ✅ erledigt (02.05.2026)
Statt WordPress-Migration: Site komplett auf statisches Express-Setup umgestellt + auf Coolify deployed. Repo: `littlelightsstudio/ferienwohnung-mistelbach`. Hetzner-DNS-A-Record auf 46.224.59.56 (Coolify) umgelenkt, NS-Switch durchgeführt, 200 OK verifiziert. easyname-Webspace für diese Domain kann gekündigt werden.

⚠️ Browser-Cache-Verdacht beim ersten Besuch nach DNS-Switch: lokaler Cache zeigt teilweise noch alte WordPress-Site, neue Site lädt korrekt via curl/Inkognito. Folge-Session: DNS-Cache-Flush + alternative Devices testen.

### Phase 3: easyname-Redirects auf Coolify migrieren (⏳ ausstehend, kritisch vor Webspace-Kündigung)
Voraussetzung für vollständige easyname-Ablösung. Hintergrund: DNS macht keine HTTP-Redirects, easyname's Webserver macht das aktuell noch. Ziel: eigener Caddy-Container in Coolify übernimmt.

**Stand:** Alle Brand-Schutz-Domains haben NS auf Hetzner umgezogen, A-Records zeigen aber weiterhin auf `77.244.243.53` (easyname-Webspace). Solange easyname-Webspace bezahlt ist, laufen die HTTP-Redirects dort. **Bei Webspace-Kündigung müssen die Redirects in Coolify (Caddy) laufen, sonst brechen Brand-Schutz-Pfade.**

**Architektur-Entscheidung (28.04.2026):** Redirects werden über ein eigenes Repo `littlelights-redirects` mit einer Caddyfile verwaltet, NICHT als Traefik-Labels in einzelnen Coolify-Apps. Begründung: alle Redirects in einer deklarativen Datei = lesbar, review-bar, von Admin in Sekunden änderbar. Caddy holt SSL eigenständig, Coolify deployt automatisch beim Push.

**Initialer Domain-Scope: 8 Brand-Schutz-Domains** (nach Drops):

| Domain | Redirect-Ziel |
|---|---|
| `nocturnedomains.com` | `helenaflinn.com` |
| `nocturnecodex.com` | `helenaflinn.com` |
| `helenaflinn-chronicles.com` | `helenaflinn.com` |
| `michaelsokolar.at` | `michaelsokolar.com` |
| `littlelights.agency` | `littlelights.studio` |
| `littlelights.at` | `littlelights.studio` |
| `littlelights.media` | `littlelights.studio` |
| `littlelights.productions` | `littlelights.studio` |

**Setup-Schritte:**

- [ ] Repo `littlelightsstudio/littlelights-redirects` anlegen (Caddyfile + Dockerfile + README)
- [ ] Coolify-Application aus dem Repo erstellen, Build-Pack `Dockerfile`, Domains hinzufügen (alle 8 plus `www.`-Varianten = 16 Einträge)
- [ ] Hetzner DNS pro Domain umstellen: A `46.224.59.56`, AAAA `2a01:4f8:1c18:e9d1::1` (statt aktuell `77.244.243.53`)
- [ ] Verifikation: `curl -I https://<domain>` muss `HTTP/2 301` mit `location:` zum Ziel liefern

**Wartung später:** Neue Redirect = 2 Zeilen in Caddyfile + DNS-Records + Domain-Eintrag in Coolify. Total ~5 Min pro Domain. **Pflege liegt bei miso (Admin)** — Lukas baut nur Tools, hat mit Server/Redirects nichts zu tun.

- Details: [`dns-zones/triage.md` Block L](dns-zones/triage.md#l-vermerk-phase-3--easyname-redirects-auf-coolify-migrieren)

### Phase 4: easyname-Registrar-Transfer + Hosting-Kündigung (🔄 in Arbeit)
- 🔄 **Registrar-Transfer Wave** läuft: littlelights.studio bei Hetzner eingereicht (siehe oben unter Stream 4 → Registrar-Transfer). 7 weitere Domains warten auf Auth-Code-Run.
- [ ] **easyname-Webhosting-Kündigung** — erst möglich nach: (a) Caddy-Redirect-Container in Coolify live, (b) helenaflinn.com auf Coolify migriert. Aktuell ist `77.244.243.53` (easyname-Webspace) noch der Redirect-Server für 6 Brand-Schutz-Domains.

---

## Offene Konzept-Fragen / Backlog

### Hauptmenü-Untermenü-Strategie (Mega-Menü)
**Status:** Konzept-Phase, Design noch nicht entschieden.

**Problem:** Sub-Bereiche (Employer Branding, Imagefilm, Werbespot, Branded Entertainment, Sustainability, Brand Documentary) sind aktuell nur via Footer erreichbar. EB ist einer der wichtigsten Bereiche und muss prominenter im Hauptmenü vertreten sein, ohne dass die Top-Level-Nav überladen wird.

**Diskutierte Richtung (28.04.):** Editorial Mega-Menü als Drawer — auf Hover/Click "Agency" öffnet ein full-width Dropdown mit Sub-Bereich-Liste links und dynamischem Visual rechts (das auf Hover des Sub-Items wechselt).

**Offene Fragen:**
- Reels & Stories — sollte das auch ein Mega-Menü bekommen? (Methodik / Showcase / Stories?) Oder bleibt Single-Link?
- Creative Studio — gleiche Frage, plus Sub-Struktur ist noch nicht definiert.
- Mobile — auf Touch-Devices wird das vermutlich ein simpleres Hamburger-Slide-In-Menü mit Accordion-Logik für die Sub-Bereiche. Konzept getrennt durchdenken.
- Hover vs Click — auf Desktop: Hover öffnet, Click navigiert zur Hub-Seite? Oder Click pflicht?

**Aufwand:** ~1h für Mega-Menü-Komponente (Desktop), zusätzliche ~1h für Mobile-Variante.

**Backend-Editierbarkeit (späterer Schritt):** Sub-Bereiche, Reihenfolge, Bilder pro Sub-Bereich und ggf. DE/EN-Labels sollen über das CMS editierbar sein. Mögliche Implementierung: Payload-Global "Navigation" mit Array-Field pro Bereich, jedes Item mit `slug`, `label`, `description`, `image` (Media-Relation). Aktuell hardcoded für Prototyp, vor Production-Launch ins CMS migrieren.

---

## Seitenstruktur (komplett)

### Hauptseiten
- Homepage
- Agency (Übersicht + Service-Unterseiten)
- Reels & Stories
- Creative Studio
- Über uns
- Kontakt
- Zusammenarbeit (Agenturpartner)

### Pflichtseiten
- ✅ Impressum (in Payload angelegt + befüllt, 02.05.2026)
- ✅ AGB (in Payload angelegt + befüllt, 02.05.2026, FAMA-referenced)
- ✅ Datenschutzerklärung (in Payload angelegt + befüllt, 02.05.2026)
- ~~Cookie-Richtlinie~~ — entfällt: mit Umami (cookieless) + keinem Tracking ohne Einwilligung ist kein eigener Cookie-Banner / -Page nötig. Der Hinweis in der Datenschutzerklärung reicht.

---

## Entscheidungslog

| Datum | Entscheidung | Kontext |
|-------|-------------|---------|
| 07.04. | Strategische Dokumente in docs/ | Klare Dokumentation statt Chat-Scrollen |
| 07.04. | EB-Marktführerschaft als zentraler Differenziator | 150+ Karrierestories, Formatentwicklung |
| 07.04. | Storytelling-Beweise statt Claims | Agency + Reels + Fantasy-Trilogie |
| 07.04. | Englischer Brand Claim bestätigt | "We make films for companies who understand the difference between content and stories worth telling." |
| 07.04. | Du-Anrede auf der Website | Professionelles Du |
| 07.04. | Branded Entertainment zu Agency | Nicht Creative Studio |
| 07.04. | Brand Storytelling eBook raus | Veraltet |
| 12.04. | Farbpalette gelockt | Navy #0f1b2d + Cream #F7F6F3 + Copper #C8956C |
| 12.04. | Satoshi als einzige Schrift | Alle Gewichte, negative Tracking bei Headlines |
| 12.04. | Diagonale als Leitmotiv | Slider, Divider, Case Study Accents |
| 13.04. | Homepage MVP gelockt | 8 Sektionen, Sticky Stacking, Footer-Reveal |
| 13.04. | Isoliert bauen, dann integrieren | Methode funktioniert, beibehalten |
| 14.04. | Projekt ist Rebranding, nicht nur Website | Website = Stream 1, Brand Collateral = Stream 2 |
| 14.04. | Phase heißt "Design" | Browser-Design mit echtem Code, kein Wireframing |
| 14.04. | Code-Variablen auf Englisch | Kommunikation Deutsch, Code Englisch |
| 14.04. | Sektionen als abstrakte Templates | Wiederverwendbar, CMS-ready, skalierbar |
| 14.04. | Bereichs-Farbschemen geplant | Agency / R&S / Creative Studio mit eigenem Farbton |
| 14.04. | "Drei Disziplinen. Eine Handschrift." | Tagline gelockt (ersetzt "Drei Bereiche") |
| 28.04. | Redirects via Caddy-Container in Coolify, eigenes Repo `littlelights-redirects` | Eine Caddyfile als Source of Truth für alle Brand-Schutz-Redirects, statt verstreute Traefik-Labels in einzelnen Apps. Lesbar, review-bar, in 5 Min pro neuer Domain erweiterbar. |
| 02.05. | Brand-Schutz "Für Agenturen" Page raus | Keine Agentur sucht das. Die Botschaft kommt durch Über Uns + Agency + R&S, braucht keine eigene Landing. Footer-Spalte "Über Uns" hat jetzt nur noch "Über Uns" + "Projekte". |
| 02.05. | AGB als FAMA-Ergänzung statt eigenständig | FAMA-AGB des Fachverbands der Film- und Musikwirtschaft Österreichs (Stand 1.1.2026) als Grundlage. Eigene AGB regulieren nur 2 Abweichungen: Feedback-Loops (2 statt 1 pro Phase) und Wettertage (50% Crew-Kompensation). FAMA-Stornogebühren übernommen. |
| 02.05. | Umami statt Google Analytics | Cookieless, DSGVO-konform out-of-the-box, self-hosted oder EU-Cloud. Keine Einwilligungspflicht, kein Cookie-Banner nötig. |
| 02.05. | Mailchimp → MailerLite | Newsletter-Stack umgestellt. EU-basiert (Litauen). |
| 02.05. | sokolar.com bleibt vorerst auf easyname-Registrar | Domains bezahlt bis Februar 2027. Mail-Forwarding-Setup ist komplex (anderer easyname-Account). Transfer optional bis Vertragsende. |
