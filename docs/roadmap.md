# Little Lights Studio — Rebranding Roadmap
**Letzte Aktualisierung: 14. Mai 2026 (Sessions 25-28: Mobile-Pass komplett — /projects + alle Single-Project-Typen + Homepage-Pyramide + Disziplin-Landing-Grid + Diagonal-Slider + Client-Logos + FooterReveal + Global Scroll-to-Top + Landscape-Phone-Nav-Hide + Hero-Animation-Footer-Fix + Dual-Path Cross-Column-Divider. Project-Tile-Primitive als wiederverwendbare Mobile-Sprache extrahiert. Mobile ist durch. Nächste Session: Resend-Kontaktformular.)**

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
| [3.4 Disziplin-Pages Skeleton](phase3/3.4_disziplin_pages.md) | ✅ Gelockt |
| [3.5 Reels & Stories Hub + Sub-Pages](phase3/3.5_reels_stories.md) | ✅ Hub + Workshop + Content-Production live (Session 14) |
| [3.6 Creative Studio Hub + Sub-Pages](phase3/3.6_creative_studio.md) | ✅ Hub + Publishing + Filme gelockt (Session 15-16) |

Gelockt:
- Farbpalette: Navy #0f1b2d + Warm Cream #F7F6F3 + Copper #C8956C
- Typografie: Clash Display (Headings) + Satoshi (Body), negative Tracking bei Headlines
- Designsprache: Hell als Basis, dunkle Sektionen für Rhythmus, Diagonale als Leitmotiv
- Homepage MVP: 8 Sektionen mit Sticky Stacking, Footer-Reveal, Lenis + GSAP
- Three-Split Slider: Diagonale Clips, Copper Divider, Hover-Expansion
- Methode: Isoliert bauen → testen → integrieren

**Bereits gebaut (Stand Session 14, 07.05.2026):**
- Hero-Variants: `full` (Homepage, animiert), `landing` (Disziplin-Hubs mit Foto + Triangle), `editorial` (Pages ohne Foto, mit/ohne Triangle), `reduced`. **Triangle-Proportionen großzügiger** (Session 14): width clamp(290px, 36vw, 580px), height clamp(140px, 16vw, 260px). Page-Title Font-Size cap clamp(1.25rem, 1.6vw, 1.55rem) für längere Page-Namen.
- Block-Library für Pages.sections: `hero`, `bold-statement`, `text-section`, `magazine-manifest` (**Small-Caps Lead-In statt Drop-Cap** seit Session 14, Field-Rename `dropCap` → `smallCapsLeadIn`), `team-grid`, `diagonal-slider`, `projects-grid`, `stats`, `faq`, `cta`, `testimonials`, `client-logos` (**Cream-Tint-Default + Hover-Color-Reveal** seit Session 14), `problem-statement`, `services-grid`, `partnership-block`, **`dual-path`** (Session 14: zwei Spalten mit Roman-Marken + Small-Caps Lead-In, Pull-Quote unten), **`framework-3x3`** (Session 14: 3 Säulen × 3 Formate Methodik-Matrix mit Selfmade/Premium/Beides Badges, formats-Array auf 0-3 flexibel), **`pricing-tiers`** (Session 14: 1-3 Tiers, Featured-Highlight, „Punkte"-Liste statt „Inklusiv-Liste"), **`process-timeline`** (Session 14: 3-7 Steps horizontal mit Disziplin-Pfeilen, optional Loop-Indicator für zyklische Prozesse, Pricing pro Step + Optional-Badge)
- **Geteilter Lead-In-Renderer** ([lib/leadInRenderer.tsx](../../littlelights-build/src/lib/leadInRenderer.tsx)) — wraps erste 3 Wörter in `.lead-words` Span für Small-Caps. Verwendet von DualPath und MagazineManifest.
- **Geteilter RichText-Converter** ([lib/richTextConverters.ts](../../littlelights-build/src/lib/richTextConverters.ts)) — `internalDocToHref` resolviert interne Links auf Projects (`/projects/[slug]`) und Pages (walked parent chain via `computePagePath`). Gilt für alle 4 RichText-Components (DualPath, MagazineManifest, TextSection, FAQ).
- **SectionDivider** automatisch zwischen adjacent **cream-cream** Blocks (Session 14 angepasst: Navy-navy braucht keinen Divider, Padding genug Trennung).
- **CTA-Button area-accent aware** (Session 14): `var(--area-accent)` statt hardcoded Copper, Hover via Opacity. Coral auf R&S, Copper auf Agency, Slate-Blue auf Creative Studio.
- Globals: `Header` (Mega-Menu) + `Footer` (5 Spalten mit auto-from-parent + manual-Modi) + `SiteSettings`
- Wiederverwendbares `FooterReveal`-Pattern für alle dynamischen Pages
- **Section-Padding einheitlich** auf clamp(64px, 9vw, 120px) — Adjacent-Sum max 240px
- Komplette Sub-Pages: **Über Uns**, **Agency-Hub**, **Employer Branding**, **Imagefilme** (Dual-Path „Inszeniert oder Dokumentarisch" hinzugefügt 07.05.), **Werbespots & Kampagnen**, **Nachhaltigkeit**, **Branded Entertainment** (07.05.), **Reels & Stories Hub**, **R&S Workshop** (07.05.), **R&S Content-Production** (07.05.), **Legal-Pages**
- EU AI Act Compliance: optionales `aiDisclosure`-Feld auf Projekten, Drafts in `docs/`

Nächste Schritte → siehe [3.3 Design Tasks](phase3/3.3_design_tasks.md). Operativ:
- TeamMembers in Payload befüllen (Photos + Hover-Photos + Socials)
- Legal-Pages anlegen + Inhalte einsetzen (Drafts liegen vor: Impressum, Datenschutz, AGB)
- Disziplin-Pages bauen — Skeleton + Block-Inventar gelockt in [3.4 Disziplin-Pages](phase3/3.4_disziplin_pages.md). Reihenfolge: Agency-Hub heute → Agency-Sub-Pages → R&S → Creative Studio. Neue Blocks werden disziplinweise gebaut, nicht vorab.
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
- ✅ **Visibility-System auf Pages-Collection** (Session 13) — Pages haben jetzt das gleiche Draft/Private/Public-Pattern wie Projects. Auth-aware Filter über `lib/visibility.ts`: anonyme User sehen nur public, eingeloggte Admins zusätzlich private. Drafts immer ausgeschlossen (kommen über Payload-Preview). `isFeatured` aus Projects entfernt. Lokaler Backfill via SQL durchgeführt. Auf Prod muss die Schema-Migration nach Deploy mit `yes` bestätigt werden, dann manueller `UPDATE`-SQL für Bestandsdaten (Details in HANDOFF).
- [ ] **Zweisprachigkeit DE/EN** — Localized-Felder sind im Schema vorbereitet, aber Routing/Switcher noch nicht gebaut
- [ ] **Kontaktformular + Calendly** (nur R&S/Workshop). Stack gelockt: **Resend** als Mail-Provider (gratis bis 3k/Monat, moderne API), API-Route `/api/contact` validiert + versendet an studio@littlelights.studio. Spam-Schutz: Honeypot-Feld + Rate-Limiting auf der Route, Cloudflare Turnstile als Option falls Volumen es erfordert. Calendly-Variante: Inline-Widget-Embed je nach CMS-Block-`variant`. Plus Success/Error-State im Formular.
- [ ] **SEO-Implementierung** — SEO-Plugin ist installiert, aber Schema Markup, Sitemap, hreflang, 301-Redirects fehlen
- [ ] **GEO-Optimierung** für AI-Suche
- [ ] **Self-Hosting der Schriften** (Satoshi, Clash Display) statt Fontshare-CDN — DSGVO-Vereinfachung (kein externer Verarbeiter), Performance-Gewinn, via `next/font/local` einbinden. Aktuell läuft via api.fontshare.com, ist im Datenschutz erwähnt
- [ ] **Markdown-Auto-Conversion im Lexical-Editor** (`MarkdownTransformersFeature`) — komfortabel für künftige Content-Edits, aktuell muss manuell im Editor formatiert werden
- ✅ **KI-Transparenz-Feld bei Projekten** (EU AI Act Art. 50, Stichtag 02.08.2026) — optionales RichText-Feld `aiDisclosure` in der Projects-Collection, wird auf der Projekt-Detail-Seite vor den Credits gerendert wenn gefüllt. Nur befüllen wenn KI substantiell im finalen Werk. Voraussetzungen liegen in `docs/ki-inventar.md`, `docs/ki-richtlinie.md`, `docs/datenschutz-ki-section.md` (letztere geht in die Datenschutzerklärung mit Anwalts-Review)

#### Agency-Hub Polish-Backlog (Stand 04.05.2026)

- [x] **Pull-Quote-Spalte breiter** im Magazine Manifest (Session 9: Spalten-Verhältnis 2.1fr/1fr → 1.7fr/1fr, min-width 220px → 280px)
- [x] **Lead-Headline-Bruch fixen** (Session 9: User direkt im CMS gepasted)
- [x] **Services-Grid Card-Title-Konsistenz** (Session 9: h3 font-size clamp(1.25rem, 1.8vw, 1.5rem) → clamp(1.2rem, 1.65vw, 1.375rem))
- [x] **`FeaturedProjectsClient` Big-Headline aus CMS** (Session 9: `bigHeadline`-Feld in `projects-grid`-Block, Default behält alten Text)
- [ ] **Mobile-Verifikation Agency-Hub** — Services-Grid, Partnership-Pillars, Projects-2x3, Magazine-Manifest mit Quote auf realem Device durchgehen

#### Sub-Pages-Build (Stand 05.05.2026)

- [x] **Employer Branding** (`/agency/employer-branding/`) — gelockt 04.05.2026. 11 Blöcke, ~1.060 Wörter, eigene Stats (150+/24/900+/12+), FAQ-Block live, Sagmeister-Quote.
- [x] **Imagefilme** (`/agency/imagefilme/`) — gelockt 05.05.2026. Bogen wie EB ohne Stats, Bold Statement „Marken, / die geglaubt werden." (final 06.05., greift Pain-Point direkt auf), Process 3-phasig (Briefing & Gespräch → Konzept 2-3 Richtungen → Wahl & Produktion), „Wo wir drehen" mit Kernteam-Handschrift-Aspekt, FAQ mit Budgetrahmen-Insight + Werbespot-vs-Imagefilm-Metapher (Einladung/Kennenlernen). Testimonials werden nachgetragen.
- [x] **Werbespots & Kampagnen** (`/agency/werbespots/`) — gelockt 06.05.2026. Bewusst kürzer (~700 Wörter), ohne Stats/Process/„Wo wir drehen". Position „Story über Spektakel". Magazine-Manifest #2 als Agentur-Block (kreativer Produktionspartner, mitdenkende Umsetzung, ohne Konzept-Wettstreit). Big Headline Projects-Grid: „Werbung, die nicht laut sein muss." Projekte trägt User selbst ein.
- [x] **Nachhaltigkeit** (`/agency/nachhaltigkeit/`) — gelockt 06.05.2026 (Session 12). Bold „Nachhaltigkeit, / ehrlich erzählt." Cases: Plastic Bank Manila + Hard Talks + Blue Plan + Sustainability Message + Strabag Sustainability Stories. Magazine #2 mit User-Insight „bewusst handeln, nicht über Nacht umdrehen — Lichtschalter abdrehen ist Symbolik, intelligente Raumsteuerung ist Wirkung." Greenwashing positiv gerahmt.
- [x] **Reels & Stories Hub** (`/reels-stories/`) — erste Version live 06.05.2026 (Session 12). Bold „Drauflos drehen / kannst du selbst." 12 Blöcke. Workshop-First-Methodik, 4 modulare Konstellationen, Pricing teil-transparent (ab 950 € Workshop, 2.500-4.500 €/Monat Setups). Christoph Masin / JägerTEE Testimonial. Reihenfolge: Pricing nach Projekten (emotional Commitment first). Konzept-Doc: [3.5](phase3/3.5_reels_stories.md).
- [x] **Imagefilme: Dual-Path-Block** „Inszeniert oder Dokumentarisch" (Session 14, 07.05.2026) — neuer wiederverwendbarer Block, Roman-Marken (I/II), Small-Caps Lead-In auf erste 3 Wörter, Diagonale-Brand-Anker. Cases als Inline-Disziplin-Links (interner SEO + RichText-Converter `internalDocToHref` für alle 4 RichText-Components).
- [x] **Branded Entertainment** (`/agency/branded-entertainment/`) — gelockt 07.05.2026 (Session 14). 7 Blöcke, ~600 Wörter. Bold „Werte, / ohne zu verkaufen." mit Tagline „für Marken, die als Publisher denken." Verlagshaus-Faden durchgehend (Lego/Patagonia/Red Bull als Beispiele). Storytelling-Wurzeln-Section ohne direkte Namensnennung (Studio-„wir" inkl. Helena Flinn Trilogie als Publisher-Beleg). Cross-Listing: Plastic Bank Manila + IRR + Allianz Paralympics zusätzlich zu Imagefilm/Sustainability hier.
- [x] **R&S Workshop-Sub-Page** (`/reels-stories/workshop/`) — gelockt 07.05.2026 (Session 14). 11 Blöcke. Bold „Vom Posten / zur Marke." Tagline „Workshop für Unternehmen, die mehr sein wollen als ein Profil." Anti-SMM-Workshop-Positionierung durch Magazine #1. Partnership-Block für 3 Säulen (vertieft gegenüber Hub: Why/Kern/Skalierungs-Kaskade implizit). 4-Karten Workshop-Ablauf. 2 Pricing-Tiers (Solo 1.500 € / Workshop+Produktion 950 € featured). FAQ + Christoph Masin Testimonial.
- [x] **R&S Content-Production Sub-Page** (`/reels-stories/content-production/`) — gelockt 07.05.2026 (Session 14). 9 Blöcke. Bold „Strategie & Story zuerst. / Bilder folgen." Tagline „Social Media Film-Produktion mit System." Process-Timeline-Block mit 4 Bausteinen als Monats-Zyklus + Loop-Indicator + Pricing pro Baustein (Konzeption ab 500 €, Drehtag ab 900 €, Postproduktion ab 800 €/Tag oder 75-150 €/Film, Betreuung ab 450 € optional). Magazine #2 mit 4 Konstellations-Beispielen narrativ.
- [x] **Creative Studio Hub** (`/creative-studio/`) — gelockt 07.05.2026 (Session 15). 7 Blöcke. Bold „Geschichten, / die uns wach halten." Voice-Pass section-by-section mit User. Magazine, Dual-Path (I Verlag / II Filme, Pull-Quote „Der Antrieb ist derselbe. Herzensprojekte, denen wir helfen, das Licht der Welt zu erblicken."), Projects-Grid (2-Col Layout, neu in Session 15), 1 Independent-Review-Testimonial. CTA „Habt ihr einen Stoff?" V1 bleibt.
- [x] **Publishing-Sub** (`/publishing` + `/creative-studio/publishing`, beide URLs aktiv via Next.js-Rewrite) — gelockt 07.05.2026 (Session 15). 7 Blöcke. Bold „Ein kleiner Verlag aus Wien. / Mit Sorgfalt gebaut." Cold-Traffic-Page für Buchleser:innen (URL in jedem Buch gedruckt). Magazine erklärt Studio-Kontext + Origin (2018 Goblins) + Operation (KDP/IngramSpark) + Position. Trilogie-Showcase. **Storyworld-Section** für helenaflinn.com. **Book-Reviews-Block (neu Session 15)**: 1 Featured (Independent Review of Books) + 5 kuratierte Stimmen (Hannah Lindley, Olson-Roy/Vienna-Freud, Jordie/Family-Read-Aloud, Mike Kren, LoveReading4Kids). CTA „Schreib uns gerne." mit Storyworld-Pointer in Subline.
- [x] **Creative Studio Filme-Sub** (`/creative-studio/short-long-films`) — gelockt 08.05.2026 (Session 16). 4 Blöcke, bewusst kurz. Bekenntnis-Page ohne konkrete Projekte. Bold „Filme, die zu uns passen. / Und wir zu ihnen." Magazine: Team (Regie/Drehbuch/Producer), Set-Erfahrung (Auftrag + eigene; Kurz/Serie/Lang), drei Wege (Förderung / Eigen-Engagement / Reife-Zeit). CTA „Schreib uns." offene Tür für Filmemacher:innen. Wird mit künftigen Filmen wachsen.
- [ ] **Workshops & Keynotes** (`/agency/workshops/`) — **Post-Launch**: User-Entscheidung 07.05.2026, zu wenig Substanz für jetzt.

#### Build-Backlog Session 9 (Stand 05.05.2026)

- [x] **EB-Sub-Page bauen** — `/agency/employer-branding/` live. 11 Blöcke, alle Texte im CMS, Stats-Block + FAQ-Block ergänzt.
- [x] **Stats-Block CMS-Felder vervollständigen** — Block-eigenes `stats[]`-Array implementiert (visible nur wenn `useGlobalStats=false`), Stats-Component zur Server-Component, lädt entweder SiteSettings oder Block-Stats. Auch in Homepage-page.tsx durchgereicht.
- [x] **`faq`-Block bauen** — Editorial Q&A-Pattern, alles offen sichtbar (kein Akkordeon, da Magazin-Lesefluss + GEO-Indexierung priorisiert), FAQPage Schema.org JSON-LD inline gerendert. Wiederverwendbar.
- [x] **Scroll-Performance auf EB-Page** — Hauptursache war `backdrop-filter: blur(16px)` im Nav.scrolled bei Background `.97` Alpha (Blur kaum sichtbar, GPU-teuer). Backdrop-filter raus + `will-change: transform` auf sticky Pull-Quote.
- [x] **Projects-Grid Logic-Fix** — `manualProjects` wurde in `RenderBlocks` gar nicht durchgereicht (Bug aus Session 9). Plus `handleShuffle` rebaselined: „Neu mischen" rotiert jetzt komplett (auch Anker), wie vom User gewünscht. Sequential Resolve statt Promise.all für garantierte Order.

#### Final-Pass-Items (am Ende, nicht pro Page einzeln)

User-Wunsch (05.05.2026): SEO/GEO-Felder und QA-Pässe nicht pro Page individuell befüllen, sondern in einem clean Pass am Ende — alle Pages und Projects aus der Datenbank holen, dann durchgängig befüllen.

- [ ] **SEO/GEO-Felder pro Page** — Title-Tag, Meta-Description, OG-Image, Alt-Texte für alle Bilder, Internal Links auf Cases. Cleaner Pass über alle Sub-Pages und Projekte am Ende.
- [ ] **Schema Markup global** — `Organization`, `Service` pro Service-Sub-Page, `VideoObject` pro Case mit Video, `BreadcrumbList`. FAQPage ist im FAQ-Block schon enthalten.
- [ ] **Mobile-Pass** durch alle Sub-Pages (Agency-Hub, EB, Imagefilme, weitere). Padding/Stacking-Korrekturen wo nötig.
- [ ] **Resend-API + Form-Submit** für CTA-Form-Variant. Stack ist gelockt, Implementation steht.
- [ ] **Restliche Agency-Sub-Pages** mit Inhalten füllen: Imagefilme (in Arbeit), Werbespots, Branded Entertainment, Nachhaltigkeit, Workshops & Keynotes

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

### Plan: diese Woche → Subdomain-Deploy mit noindex

**User-Vereinbarung 07.05.2026 (Session 14):** Ziel ist diese Woche die Page so weit zu bringen, dass nächste Woche das Team in Ruhe testen + Feedback geben kann. Erster Deploy auf eine Staging-Subdomain mit X-Robots-Tag noindex global.

**Diese Woche (07.05.-10.05.2026):**
- [x] Branded Entertainment (Agency-Sub-Page) — done Session 14
- [x] R&S Workshop-Sub-Page — done Session 14
- [x] R&S Content-Production-Sub-Page — done Session 14
- [x] **Creative Studio Hub + Publishing-Sub** — gelockt Session 15 (07.05.)
- [x] **Creative Studio Filme-Sub** — gelockt Session 16 (08.05.)
- [x] Logo-Hover Color-Reveal — done Session 14
- [ ] **Alle Projekte mit Content befüllen** (Videos + Fotos) — Userarbeit, großer Sicht-Durchgang
- [ ] **Staging-Subdomain Deploy** — `staging.littlelights.studio`, X-Robots-Tag noindex global, gleiche DB wie Prod (User-Entscheidung 07.05.)
- [ ] ~~Lean /kontakt-Page~~ — verschoben auf Post-Push, nicht launch-blockierend (User 08.05.)
- [ ] ~~404-Page~~ — verschoben auf Post-Push, nicht launch-blockierend (User 08.05.)

**Translation-Pipeline (Session 17–18, 09.05.2026):**
- ✅ `scripts/export-pages-to-md.py` gebaut (Session 17) — Spiegel zur Projects-Pattern, alle 20 Block-Types abgedeckt, RichText (inkl. nested Quotes/Lists) extrahiert sauber.
- ✅ **Autonomer Translation-Run durchgelaufen (Session 18, 09.05.)** — alle 18 Pages (außer Workshops-Keynotes post-launch) und 43 Projects in DE+EN inkl. SEO + GEO-Questions. Mechanik: 2-Step-Workflow per REST PATCH (DE für SEO/geoQuestions/schemaType + EN für sections + EN-Übersetzungen). Decision-Log und Probleme in `docs/exports/translation-decisions.md` und `docs/exports/progress.md`.
- ⚠️ **Kritischer Lerneffekt aus Session 18**: Niemals partielle `sections: [{einzelner-Block}]`-PATCHes senden — Payload behandelt sections-Array als Complete-Replace, nicht als Merge-by-ID. Beim Bug-Fix-Versuch sind Home/Agency/EB/Workshop temporär auf 1 Section kollabiert, vollständig restored aus den Initial-Snapshots. Plus: nested-array Item-IDs müssen exakt match'en zwischen DE-Snapshot und EN-Build-Body, sonst entstehen verwaiste Items.

**Erledigt seit letzter Roadmap-Aktualisierung:**
- [x] **Staging-Deploy live** auf staging.littlelights.studio mit X-Robots-Tag noindex + Let's Encrypt (Session 19, 10.05.). Coolify-App + Postgres-Service + Bind-Mount für Media, GitHub-Repo `littlelightsstudio/littlelights-build` als Source of Truth. Beim Cutover wird `littlelights.studio` als zweite Domain auf dieselbe App geroutet (eine DB, zwei Domains).
- [x] **404-Page** als Polaroid-Card mit Random-Bild aus `SiteSettings.notFound`-Galerie (Session 19). Headline/Body/CTA/Galerie alle CMS-driven und localized.
- [x] **Mobile-Nav (Hamburger-Drawer)** (Session 20-22). Slide-in von rechts mit cream BG, Areas expandierbar mit Sublevel-Thumbnails, Brand-Signature mit Tap-to-Fill Gradient am Drawer-Bottom, CTA als Sticky-Footer. Hamburger als prominenter Disziplin-Color-Chip (Copper/Terracotta/Blue-Grey). Row-Split: Label-Link zur Hub-Page + Chevron-Toggle für Sublevel-Aufklappen.
- [x] **Footer-Mobile-Layout** (Session 20-22) — 5-Spalten-Grid auf 375px war unleserlich, jetzt zwei unabhängige Flex-Stacks (links Agency + R&S, rechts Creative Studio + Über Uns + Kontakt). Footer-Bottom (Socials, Legal, Copyright) zentriert.
- [x] **Umami Web-Analytics selfhost** (Session 20-21) auf `analytics.littlelights.studio` (Coolify-Service-Template mit bundled Postgres). Zwei Websites registriert (staging + prod), Tracking-Script in `layout.tsx` mit hostname-basiertem ID-Picker. Erste Pageviews live verifiziert.
- [x] **Mobile-Pass Sub-Pages erste Welle** (Session 23, 12.05.) — Sub-Page-Header (Editorial + Landing) mit Triangle-Tuning, Homepage-Hero mit Reveal-from-below + Logo-Position, Hamburger 36×36 zentriert, BoldStatement-Counter-Lesbarkeit beim Color-Fill, MagazineManifest-Pull-Quote-Stack auf Mobile, Testimonials-Grid-Layout + Slant-Removal + Headline-Rebrand „Stimmen über uns", ServicesGrid-Top-Padding. Screenshots waren von minimiertem Browser — Session 24 hat das auf realem iPhone nachjustiert.
- [x] **Mobile-Pass Real-Device-Tuning** (Session 24, 13.05.) — auf realem iPhone 14-Pro durchgegangen: Sub-Page-Triangle in zwei Iterationen je 10% kalibriert (final clamp(146px, 39vw, 194px)), Notch differenziert (Editorial 56px Copper-Konflikt, Landing 24px), Nav-Padding symmetrisch (16px beidseitig), Page-Title-Font für lange Titel reduziert, Stats-Grid 4-Spalten → 2×2 auf Mobile, Stats-Label/BoldStatement-Tagline Opacity .2-.25 → .5 (WCAG-AA), ProblemStatement-Padding `48px` → `clamp(16px, 4vw, 48px)` damit „Beschäftigungstherapie" zentriert reinpasst, Horizontal-Scroll-Lock global (`overflow-x:hidden` auf html+body, `touch-action: pan-y`) gegen FooterReveal-Slide-Bug.
- [x] **/projects-Page Mobile-Redesign** (Session 24, 13.05.) — Pyramide-Filter (3 Zeilen 3-2-2 mit Gradient-Fades als Verbindung), 2-col Square-Grid mit Case-Study-Span-2-Anker, ScrollToFilter-FAB nach 400px Scroll. Ansatz steht, Fine-Tuning für nächste Session.
- [x] **Mobile-Pass komplett — Sessions 25-28** (13.-14.05.) — alle Project-Page-Typen (Overview, Single Hochformat/Landscape/Case-Study), Homepage-Pyramide (1+2+2 mit display:contents Row-Kollaps + Drop der 6. Card), Disziplin-Landing-Equal-Grid (uniform 2-col 1:1, Title fix 14px), DiagonalSlider (Tap-State activeIndex, expandierte Spalte + zwei kollabierte Strips mit rotierten Labels entlang vertikaler Brand-Diagonale), Client-Logos (flex-wrap + justify-center, 2 zentrierte Zeilen), Dual-Path (Cross-Column-Divider raus auf Mobile — Roman-Marks tragen Trennung selbst), Hero-Animation-Footer-Flash (Bold-Statement von Anfang sichtbar statt 3s Dissolve). Project-Tile-Primitive (`project-tile-grid`/`project-tile`/`size-hero`/`tile-hide-mobile`) als wiederverwendbare Mobile-Sprache extrahiert und überall angewandt. Plus FooterReveal global auf /projects + /projects/[slug] eingehängt (war dort nie gemountet). ScrollToTop FAB global in layout.tsx ersetzt den filter-spezifischen FAB. Mobile-Cursor disabled auf Touch-Devices. Landscape-Phone Nav-Hide via `(max-height:500px) and (orientation:landscape)`.

**Nächste Schritte (in Reihenfolge):**
1. **Resend-Kontaktformular** (Session 29) — API-Route POST /api/contact, Resend SDK, Spam-Schutz (Honeypot + Rate-Limit, evtl. Cloudflare Turnstile), Zod-Validation, Success/Error-States. CTA-Form ist seit Session 15 statisch CMS-driven, Submit-Logik fehlt.
2. **DE/EN Routing/Switcher** — Übersetzungs-Content liegt in beiden Locales sauber vor (Session 18). Jetzt fehlt das Frontend: Locale-Detection, URL-Pattern (`/en/...`), Switcher in Header/Footer, hreflang-Tags. Slug-Strategie gelockt: Option A (DE-Slugs für beide Locales). EN-Variante für Publishing-Sub priorisiert (Cold-Traffic aus Büchern). ~1 Tag.
3. **Hero-Anchor-Verifikation** — User-Feedback Session 28: "anchor stimmt nicht ganz" nach Wegfall des Statement-Slide-ins. Visuell prüfen, ob Statement-marginTop:-40 in Verbindung mit Hero-Shrink (100vh → 100vh-80) noch sauber sitzt.
4. **Restliche Mobile-Items** — iPad Mega-Menu-Position (820px-Portrait), Book-Reviews auf Mobile, 404-Page-Check.

**Danach (Team-Feedback-Phase):**
- [ ] **ESLint + TypeScript Build-Gates wieder aktivieren** — beim Staging-Deploy ad-hoc deaktiviert in `next.config.mjs` (`eslint.ignoreDuringBuilds`, `typescript.ignoreBuildErrors`). 5 ESLint-Errors (3× `<a>` → `<Link>`, prefer-const, unused-expression) + Payload-API-Updates in `regenerate-media/route.ts`.
- [ ] **Self-Hosting Fonts** (Satoshi, Clash Display) via `next/font/local` — DSGVO-Vereinfachung
- [ ] **SEO/GEO Final-Pass** — Title, Meta, OG-Image, Alt-Texte über alle Pages
- [ ] **Schema Markup global** — Organization, Service, VideoObject, BreadcrumbList
- [ ] **Media-Performance** — Caddy/nginx als Static-File-Server vor Payload, oder S3-Adapter mit CDN. Bisher Quick-Win nur Cache-Control-Header (max-age=2592000) via Middleware
- [x] **Slider-Polish** — DiagonalSlider Mobile auf Tap-State umgebaut (Session 27), Desktop Hover unverändert. Cop-Divider-Positionierung war Desktop-Only-JS, auf Mobile via display:none neutralisiert.
- [ ] **Lean /kontakt-Page** (404-Page ist seit Session 19 live)
- [ ] **Restliche Launch-Items** — siehe Phase 6

**Post-Launch / Backlog:**
- [ ] Workshops & Keynotes (Agency-Sub-Page) — Substanz erst aufbauen
- [ ] Brand Documentaries als eigene Page — wenn 5+ Cases vorliegen
- [ ] Calendly-Integration
- [ ] **Umami Custom-Events** — Click-Tracking auf CTAs, Form-Submits, Filter-Nutzung. Bewusst NACH 1-2 Wochen Live-Traffic, wenn klar ist welche Conversion-Punkte zählen

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
