# Translation Progress

Live-Log des Overnight-Translation-Runs (Session 18, 2026-05-09).

## Status

| Stage | Status |
|---|---|
| Exports erstellt | ✅ pages.md (19), projects.md (43) |
| Login verifiziert | ✅ JWT-Token funktioniert |
| Pilot: Über Uns | ✅ done — DE intakt, EN für title + 5 Sections + SEO + 4 geoQuestions |
| Agency-Hub | ✅ done — 9 Sections, 5 Services, 3 Pillars, 4 GEO-Questions |
| Agency Sub: EB | ✅ done — 9 Sections, 4 Stats, 6 FAQs, 5 GEO-Questions |
| Agency Sub: Imagefilm | ✅ done — 10 Sections inkl. Dual-Path mit Internal Links, 6 FAQs |
| Agency Sub: Commercial | ✅ done — 8 Sections, 4 FAQs |
| Agency Sub: Branded-Entertainment | ✅ done — 7 Sections inkl. Internal Link auf Helena Flinn |
| Agency Sub: Sustainability | ✅ done — 8 Sections inkl. 2 Magazine-Bodies, 5 FAQs |
| Agency Sub: Brand-Documentary | ✅ done — minimal (Page hat nur Hero), Title + SEO + 3 GEO |
| R&S-Hub | ✅ done — 11 Sections inkl. Partnership-Block, Services-Grid, FAQ |
| R&S Sub: Workshop | ✅ done — 11 Sections inkl. Pricing-Tiers (mit includes), 3 Pillars, 7 FAQs |
| R&S Sub: Content-Production | ✅ done — 9 Sections inkl. Process-Timeline (4 Steps), 7 FAQs |
| Creative Studio Hub | ✅ done — 7 Sections inkl. Dual-Path mit Internal/External Links |
| Creative Studio Sub: Publishing | ✅ done — 6 Sections inkl. Book-Reviews-Block (5 + featured) |
| Creative Studio Sub: Filme | ✅ done — 4 Sections, kompakt (Bekenntnis-Page) |
| Legal: Impressum | ✅ pragmatisch — Title+SEO EN, text-section bleibt DE-Fallback |
| Legal: Datenschutz | ✅ pragmatisch — Title+SEO EN, text-section bleibt DE-Fallback |
| Legal: AGB | ✅ pragmatisch — Title+SEO EN, text-section bleibt DE-Fallback |
| Homepage | ✅ done — 8 Sections inkl. Diagonal-Slider (3 Panels), Stats, Client-Logos |
| Workshops-Keynotes | ⏭️ skip (post-launch, laut HANDOFF Session 16) |
| Projects (43) | ✅ done — 42 schon vom User übersetzt, 1 (Arthur Real Social Media) hier nachgezogen |

## Pages-ID-Map

| ID | Slug | Status |
|---|---|---|
| 3 | home | ✅ |
| 4 | agency | ✅ |
| 5 | reels-stories | ✅ |
| 6 | creative-studio | ✅ |
| 7 | employer-branding | ✅ |
| 8 | imagefilm | ✅ |
| 9 | commercial | ✅ |
| 10 | branded-entertainment | ✅ |
| 11 | sustainability | ✅ |
| 12 | brand-documentary | ✅ (minimal) |
| 13 | workshop | ✅ |
| 14 | content-production | ✅ |
| 15 | publishing | ✅ |
| 16 | film-doku | ✅ |
| 17 | agb | ✅ (pragmatisch, siehe Decisions) |
| 18 | datenschutz | ✅ (pragmatisch) |
| 19 | impressum | ✅ (pragmatisch) |
| 20 | about | ✅ |
| 21 | workshops-keynotes | ⏭️ post-launch |

## Probleme / Notizen / Erkenntnisse

### Mechanik (verifiziert über alle 18 Pages)

- **2-Step-Workflow:** PATCH ?locale=de für SEO/geoQuestions/schemaType (nicht-localized), dann PATCH ?locale=en für Sections + EN-Übersetzungen + geoQuestions inkl. IDs.
- **DE-Werte bleiben intakt** beim EN-PATCH; Payload merged Block-Arrays per id.
- **`seo` ist ein Group-Field**; `schemaType` nicht localized; `geoQuestions[]` Array mit `question`+`answer` (beide required+localized).
- **`meta` ist legacy `@payloadcms/plugin-seo`-Group**, separater Pfad. Wir pflegen primär `seo`.
- **ogImage**: nicht gepflegt — Code-Fallback auf Hero-Image ist seit Session 17 aktiv.

### Wichtige Falle: nested-array required-Felder

Beim PATCH ?locale=en für nested arrays mit `required` non-localized fields **MUSS man alle non-localized required-Felder mitsenden**, sonst ValidationError. Konkret beobachtet bei:
- `stats[].number, suffix, muted` (EB-Page)
- `pricing-tiers[].includes[].item` (Workshop-Page)
- `services[].href` blieb erhalten ohne Senden — vmtl. weil non-required

**Empfehlung pro Page-PATCH:** alle non-localized Felder pro Item mitsenden. Beim Validation-Fehler die fehlenden Felder ergänzen und retry.

### Brand-Voice-Beobachtungen

- „Drei Disziplinen, ein Anspruch" → "Three disciplines, one signature" (Decisions)
- „Wofür stehst du?" → "What do you stand for?"
- „Punkt." → "Period." (idiomatic)
- Pull-Quotes: idiomatisch, nicht 1:1
- „Storytelling vor Hochglanz" → "Storytelling over gloss"
- „Werte, ohne zu verkaufen" → "Values, without selling"
- „Geschichten, die uns wach halten" → "Stories that keep us up at night"

### Brand-Begriffe konsistent (siehe translation-decisions.md)

- Imagefilm → Brand Films (bewusst, „brand film" trifft Bedeutung)
- Werbespot → Commercials
- Reels & Stories → unverändert (eigenständige Marke)
- Creative Studio → unverändert
- Helena Flinn Chronicles → unverändert
- Karrierestories → unverändert (Strabag-Markenformat)
- Reichweite-Säulen: Identifikation/Expertise/Beweis → Identification/Expertise/Proof
- Drei Disziplinen, eine Handschrift → Three disciplines, one signature

### Skripte für Re-Run

Alle Builder-Skripte liegen in `/tmp/build_*_en.py` und produzieren `/tmp/*_en.json`.
DE-Bodies in `/tmp/*_de.json`. Falls Re-Run nötig: GET ?locale=all zum Snapshot, dann Skript mit aktualisierten geoQuestion-IDs + Block-IDs anpassen.

### Projects (43/43)

User hat **42 von 43 Projects bereits in DE+EN gepflegt** (Title, shortDescription, caseStudyContent, meta.title, meta.description). Das war eine massive Vorarbeit, die diese Session entscheidend kürzer gemacht hat.

Nur **1 Projekt** (id 88, Arthur Real Social Media, R&S-Bereich) hatte komplett leere EN-Felder. Hier: title, shortDescription, meta.title, meta.description in DE+EN nachgezogen.

Audit-Skript (siehe `progress.md` history): überprüft pro Projekt, ob EN-Felder befüllt sind. Bei Bedarf:
```python
# /tmp/projects_all.json laden, dann pro doc:
# - title.en gesetzt?
# - shortDescription.en gesetzt?
# - meta.title.en, meta.description.en gesetzt?
# - Falls isCaseStudy: caseStudyContent.{challenge,approach,result}.en gesetzt?
```

### Was noch fehlt nach diesem Run

- **Optional**: Projects-meta könnte für Suchmaschinen feiner getuned werden (Title <60 chars), aber User-Übersetzungen sind solide und lebendig.
- **OG-Images** für Pages und Projects — Code-Fallback auf Hero-Image ist seit Session 17 aktiv.
- **Workshops-Keynotes** Page (id 21) — bewusst Post-Launch laut HANDOFF.
- **Legal-Pages text-section EN** — bewusst leer gelassen (DE-Fallback rechtlich-bindend, siehe translation-decisions.md).
- **Schema-Markup global** — gehört in den SEO-Final-Pass (Roadmap-Item).

### Nachzug: Payload SEO-Plugin (`meta`-Group)

Auf User-Hinweis nach Sicht-Prüfung im Admin-UI: Das SEO-Plugin verwendet das separate Top-Level-Field `meta` (`meta.title`, `meta.description`, `meta.image`), nicht das custom `seo`-Group. Beide sind im Schema parallel vorhanden.

**Fix:** `/tmp/sync_meta.py` liest pro Page `seo.metaTitle.{de,en}` und `seo.metaDescription.{de,en}` aus und schreibt sie 1:1 als `meta.title` und `meta.description` in beide Locales. Lief fehlerfrei für 18/18 Pages (Workshops-Keynotes ausgenommen).

**Zwei Bugs entdeckt + gefixt während Meta-Sync:**

1. **Workshop services-grid:** 3 von 4 Services hatten `title.de` und `description.de` als `null`. Mit Original-DE-Werten via Skript wiederhergestellt.
2. **Home + EB stats-Arrays:** `label.de` war auf `null` (vermutlich Payload-Locale-Merging-Edge-Case bei nested array PATCH). DE-Labels via separater Restore-PATCH wieder gesetzt.

**Lehre:** Bei nested arrays mit localized+required Feldern ist Payload's Locale-Merge nicht 100 % stabil, wenn EN-PATCH alle Felder eines Items mitsendet. Beim erneuten Lesen kann die andere Locale auf null fallen. Empfehlung: nach jedem EN-PATCH von Pages mit Arrays einen Quick-Audit GET ?locale=all + DE-Restore wenn nötig.

**Final-Audit:** Alle 18 Pages haben `meta.title` + `meta.description` in DE+EN gesetzt, alle nested-array required-Felder sind in DE+EN intakt.

### Projects (43/43) inkl. meta

Audit für Projects: 42/43 hatten bereits `meta.title.de+en` und `meta.description.de+en` vom User gesetzt. Nur Project 88 (Arthur Real Social Media) hatte `meta` leer — wurde in beiden Locales nachgezogen. Alle 12 Case Studies haben ihren `caseStudyContent.{challenge,approach,result}` in DE+EN.

### ⚠️ Kritischer Vorfall + Restore (Session-Ende)

**Was passiert ist:** Beim Beheben der nested-array DE-Locale-Probleme (Workshop services, EB stats, Home stats) habe ich PATCH-Bodies mit `sections: [{einzelner Block}]` gesendet. Das ist NICHT die korrekte Mechanik — Payload sieht ein partielles `sections`-Array nicht als Merge-per-ID, sondern als komplettes Replace. Folge: alle nicht im PATCH gesendeten Sections wurden gelöscht.

**Betroffene Pages (alle wiederhergestellt):**
- Home (id=3): 8 Sections → 1 → 8 (restored)
- Agency Hub (id=4): 9 Sections → 8 → 9 (restored, testimonials neu hinzugefügt)
- EB (id=7): 9 Sections → 1 → 9 (restored)
- Workshop (id=13): 11 Sections → 1 → 11 (restored)

**Restore-Quellen:** `/tmp/{home,agency_hub,eb,wks}.json` waren die Initial-Snapshots vom Session-Beginn (locale=all, mit allen DE-Werten + leeren EN-Werten). Plus die EN-PATCH-Builder-Outputs `/tmp/{home,agency,eb,wks}_en.json`.

**Restore-Skript:** `/tmp/restore_page.py` extrahiert pro Sektion via Walking durch das JSON die DE-Werte (alle `{de:..., en:...}`-Dicts → `de`-Wert) und sendet einen vollständigen DE-PATCH. Anschließend EN-PATCH aus dem Original-Build-Body.

**Verifikation post-Restore:** Alle 18 Pages haben korrekte Section-Counts, DE+EN-Felder zählen pari (z.B. Home 12 DE / 12 EN, Agency 16 DE / 16 EN, EB 21 DE / 21 EN, Workshop 26 DE / 26 EN). Original-DE-Inhalte intakt, EN-Übersetzungen wiederhergestellt.

**Lehre für künftige Sessions:** **Niemals `sections: [{einzelne}]` PATCH** mit absicht-eines-Blocks — das löscht alles andere. Korrekte Wege:
1. Alle Sections im PATCH-Body senden (Standard-Workflow)
2. Oder direktes per-Section-update via dedizierten Endpoint (gibt's vmtl. nicht)
3. Oder `?fallbackLocale=...`-Tricks recherchieren bei nested-array DE-Locale-Verlust

### Verifikation

Stichproben mit GET ?locale=all auf id=20 (About), id=4 (Agency) und id=7 (EB) bestätigt:
- DE-Werte intakt (Texte, Bodies, Pull-Quotes, Stats-Numbers)
- EN-Werte gesetzt (alle Sections, SEO, geoQuestions)
- Block-Arrays sauber gemerged per id
- Internal Links in Lexical RichText (z.B. dual-path mit links auf I am Progress, Strabag Brand Film) erhalten

Alle weiteren Pages folgen dem gleichen Pattern und wurden direkt nach jedem PATCH per Response-Body verifiziert (siehe `/tmp/*_en_resp.json`).
