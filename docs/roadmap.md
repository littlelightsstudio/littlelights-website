# Little Lights Studio — Rebranding Roadmap
**Letzte Aktualisierung: 14. April 2026**

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
- Typografie: Satoshi, negative Tracking bei Headlines
- Designsprache: Hell als Basis, dunkle Sektionen für Rhythmus, Diagonale als Leitmotiv
- Homepage MVP: 8 Sektionen mit Sticky Stacking, Footer-Reveal, Lenis + GSAP
- Three-Split Slider: Diagonale Clips, Copper Divider, Hover-Expansion
- Methode: Isoliert bauen → testen → integrieren

Nächste Schritte → siehe [3.3 Design Tasks](phase3/3.3_design_tasks.md)

### Phase 4: Build
**Ausstehend — nach Design-Abschluss**

- Payload CMS Setup + Content-Types
- Next.js 15 Frontend-Entwicklung
- CMS-Integration aller Design-Komponenten
- Zweisprachigkeit DE/EN
- Video-Integration (Vimeo/Bunny.net)
- Kontaktformular + Calendly (nur R&S/Workshop)
- SEO-Implementierung (Schema Markup, Sitemap, hreflang, Redirects)
- GEO-Optimierung

### Phase 5: Content
**Ausstehend — parallel zu Build**

- Finaler Copytext (auf Basis der Messaging-Architektur)
- 5 Full Case Studies einpflegen
- 10-15 Minimal-Ansicht Projekte
- Testimonials einholen und einpflegen
- Team-Fotos und Bios
- Bildmaterial und Video-Embeds
- Kundenlogos (SVG, farblich angepasst)

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

### DNS-Migration easyname → Hetzner DNS (🔄 in Arbeit)
21 Domains. Strategie: erst alle Hetzner-Zonen aufbauen + verifizieren, dann kontrollierter Cutover Domain-für-Domain.

- ✅ Pilot `nocturnedomains.com` in Hetzner importiert + verifiziert
- ✅ Cleanup-Konventionen etabliert ([`dns-zones/README.md`](dns-zones/README.md))
- ✅ Triage-Runde abgeschlossen ([`dns-zones/triage.md`](dns-zones/triage.md))
- ✅ DKIM-Werte für alle 4 Google-Workspace-Domains aus Google Admin Console gesammelt
- ✅ **Alle 21 Zone-Files generiert** (inkl. Cleanup, DKIM, DMARC, Cross-Domain-Auth)
- ✅ **Alle 21 Zonen in Hetzner DNS importiert** (Stand 27.04.2026, Record-Counts verifiziert)
- ✅ **Erster Cutover erfolgt:** `nocturnecodex.com` NS bei easyname auf Hetzner umgestellt (27.04.2026)
- 🤖 **Verifikations-Routine geplant:** 2026-04-29 10:00 — Zone-Integrity + NS-Propagation aller 21 Domains ([Routine](https://claude.ai/code/routines/trig_016uJCBYvToVXiTvJauiSigs))
- [ ] Cutover-Phase fortsetzen: Domain für Domain NS umstellen (Bulk-Brand-Schutz zuerst, `littlelights.studio` zuletzt)
- [ ] sokolar.com Subdomain-Cleanup-Session (separate Triage, optional vor oder nach Cutover)

### WordPress-Migration ferienwohnung-mistelbach.at (⏳ ausstehend)
Aktive WordPress-Installation auf easyname-Webspace. **Eigenes Projekt**, getrennt von DNS-Migration. DNS migriert: A-Record bleibt erst auf `77.244.243.53` damit WordPress weiterläuft.

- [ ] Neuen Host wählen (Hetzner Webspace? Coolify mit WP-Container?)
- [ ] Files + MySQL-DB exportieren und auf neuem Host aufsetzen
- [ ] DNS-A-Record umlenken
- [ ] easyname-Webspace für diese Domain abkündigen

### Phase 3: easyname-Redirects auf Coolify migrieren (⏳ ausstehend)
Voraussetzung für vollständige easyname-Ablösung. Hintergrund: DNS macht keine HTTP-Redirects, easyname's Webserver macht das aktuell noch. Ziel: eigener Caddy-Container in Coolify übernimmt.

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

### Phase 4: easyname-Registrar-Transfer + Hosting-Kündigung (⏳ ausstehend)
- [ ] Phase 2 der Domain-Migration: Registrar-Transfer easyname → Hetzner Domains (siehe domain-migration.md)
- [ ] easyname-Webhosting kündigen (erst nach WordPress-Migration + Redirect-Migration)

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
- Impressum
- AGB
- Datenschutzerklärung
- Cookie-Richtlinie (falls benötigt — bei Umami ggf. nicht nötig)

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
