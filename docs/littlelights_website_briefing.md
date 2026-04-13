# Little Lights Studio — Website Redesign Briefing
**For Claude Code | Version 1.0 | April 2026**

---

## Wichtiger Hinweis zur Arbeitsweise

Dieses Briefing ist in drei Phasen aufgebaut. **Phase 1 (Analyse) muss vollständig abgeschlossen und mit dem Auftraggeber besprochen sein, bevor Phase 2 beginnt. Phase 2 muss abgeschlossen sein, bevor eine einzige Zeile Code oder Frontend geschrieben wird.**

Nach jeder Phase: Output präsentieren, Feedback einholen, dann weitermachen.

---

## 1. Unternehmenskontext

**Little Lights Studio GmbH** ist eine Wiener Brand-Film-Agentur und Filmproduktionsfirma mit 11 Jahren Erfahrung. 8-köpfiges Kernteam, aufgeteilt in drei Bereiche:

**Agency** (Kerngeschäft)
Direkte Kundenarbeit mit größeren Unternehmen. Imagefilme, Employer-Branding-Kampagnen, TVCs, CSR-Kommunikation, Brand Documentaries, Erklärfilme, Fotoproduktion. Strategischer Partner, nicht reiner Dienstleister. Langfristige Kundenbeziehungen mit Rahmenverträgen und wachsendem Footage-Archiv.
Aktuelle Hauptkunden: Strabag (größter Kunde, laufende Karrierestories-Serie seit 2023, 100+ Episoden), Volksbank, Greiner, Austrian National Tourist Office (Österreich Werbung), Allianz, MacroArrayDiagnostics.
Zielgruppe: Corporate Communications, Marketing & Brand Management, HR/People & Culture, CSR-Abteilungen in mittleren bis großen Unternehmen.

**Reels & Stories** (im Aufbau)
Social Media Content Production für KMUs. Positionierung: keine spontanen Handyvideos, sondern deliberate moving image communication mit Strategie und Konzept. Abo-Modell mit regelmäßigen Produktionstagen. Schlanker Ansatz: 1 Videograf, kompaktes Setup. Einstieg über geführten Content & Storytelling Workshop. Preisrahmen: ca. 2.000 bis 3.500 Euro/Monat je nach Paket.
Zielgruppe: KMUs mit ernsthaftem Social-Media-Ziel (Sichtbarkeit, Recruiting, Markenaufbau), die bisher entweder nichts produzieren oder mit Smartphone-Content nicht weiterkommen.

**Creative Studio / Independent** (dritter Bereich, noch ohne finalen Namen)
Kreativere Projekte, die nicht ins Agenturgeschäft fallen: Dokumentarfilme, Kurzfilme, Filmförderungsprojekte. Publishing: Little Lights Studio ist Verlag, Michael Sokolar (CEO) ist als Autor sichtbar. Zwei Bücher bereits veröffentlicht, Middle-Grade-Fantasy-Trilogie in Arbeit. Dieser Bereich bringt wenig Umsatz, positioniert das Studio aber als Storyteller-Brand mit kreativer Tiefe.

**Strategische Ausgangssituation**
Das Agenturgeschäft ist wirtschaftlich dominant, aber zu abhängig von wenigen Großkunden. Reels & Stories soll neue, regelmäßige Einnahmen durch eine breitere Zielgruppe bringen. Die Positionierungsfrage "Agentur oder Produktionshaus" ist entschieden: Little Lights ist eine Agentur und sucht aktiv Direktkunden. Das klassische Agenturpartner-Geschäft (Subcontracting) läuft aus.

**Differenzierung**
- Emotionales Storytelling trifft strategische Markenkommunikation
- Authentische Performances durch entspannte, druckfreie Sets auch mit Nicht-Profis
- Langfristige Partnerschaft statt Einzelprojekte; lebende Footage-Archive
- B2B-Kommunikation, die wirklich engagiert

---

## 2. Ziele der neuen Website

**Primäres Ziel:** Lead-Generierung. Konkret: Anfragen für ein erstes Gespräch. Kein direkter Verkauf, keine Pakete buchbar, kein Shop. Der Kontakt ist der Conversion-Punkt.

**Sekundäre Ziele:**
- Klare Positionierung als Agentur (nicht Produktionsdienstleister)
- Reels & Stories als eigenständiges Angebot sichtbar machen und Leads generieren
- Bestehendes Portfolio als Case Studies präsentieren (nicht nur als Video-Showreel)
- Vertrauen bei Neukunden aufbauen durch Referenzen, Projekttiefe und klare Kommunikation
- Zweisprachig (Deutsch primär, Englisch als wählbare Variante, kein automatischer Übersetzer)

**Was die Website nicht ist:**
- Kein Recruiting-Hub (wird über andere Kanäle gemacht)
- Kein Kundenbereich / Login-Bereich
- Kein Blog (würde nicht regelmäßig bespielt werden)
- Kein Newsletter

---

## 3. Technische Anforderungen

- **Framework:** Offen für Vorschlag von Claude Code, bevorzugt modernes, wartungsarmes Setup
- **CMS:** Pflicht. Der Auftraggeber muss selbst Projekte als Case Studies hinzufügen, Team-Seiten anpassen, und bei Bedarf Unterseiten anlegen können — ohne Programmierer
- **Zweisprachigkeit DE/EN:** Texte werden manuell gepflegt (kein automatischer Übersetzungsservice). Beide Sprachversionen werden doppelt eingepflegt.
- **Video-Handling:** Kein selbst-gehostetes Video. Integration über Vimeo oder YouTube. Videos müssen zuverlässig in verschiedenen Formaten (16:9, 9:16) darstellbar sein, ohne bei Updates zu brechen.
- **Responsiveness:** Desktop, Tablet, Mobile vollständig
- **Barrierefreiheit:** Good practice (Kontraste, Schriftgrößen, Alt-Tags), aber keine zertifizierte Vollbarrierefreiheit erforderlich
- **SEO-Basis:** Meta Title, Meta Description, Heading-Struktur, Bild-Alt-Tags, saubere URL-Struktur
- **Kontakt:** Kontaktformular + E-Mail + Telefon. Kein Chatbot. Calendly optional, wird in Phase 2 entschieden.
- **Performance:** Ladezeiten müssen stimmen trotz Video-Content. Lazy Loading, optimierte Assets.
- **Hosting:** Wird vom Auftraggeber selbst geregelt

---

## 4. Seitenstruktur (Ausgangshypothese für Phase 2)

Dies ist eine Hypothese, keine Entscheidung. Phase 1 kann diese Struktur verändern.

```
Homepage (/)
├── Agency (/agency)
│   ├── Employer Branding Films (/agency/employer-branding)
│   ├── Brand & Image Films (/agency/brand-films)
│   ├── [weitere Service-Unterseiten nach Bedarf]
│   └── Projects / Case Studies (/agency/projects/[slug])
├── Reels & Stories (/reels-stories)
│   └── [Case Studies / Beispiele]
├── Creative Studio (/creative-studio) [Name TBD]
│   └── [Projekte: Film, Publishing]
├── About (/about)
│   └── Team
├── Contact (/contact)
└── Legal (Impressum, Datenschutz, Cookies)
```

**Wichtig für Case Studies:** Jedes Projekt soll als echte Case Study funktionieren, nicht nur als Video-Embed. Template-Felder: Video, Begleittext, Credits, Fotos, Projekthintergrund. Auftraggeber muss neue Projekte selbst anlegen können.

---

## 5. Inhaltliche Prinzipien

- **Lead mit Storytelling und Strategie, nicht mit Produktionscapabilities.** Nicht "Wir machen Imagefilme", sondern was die Filme für Kunden bewirken.
- **Kein Agency-Cliché.** Keine "passionate team of creatives", keine "cutting-edge solutions", keine leeren Superlative.
- **Pain vor Lösung.** Was ist das konkrete Problem des Kunden, bevor wir über unsere Leistungen sprechen?
- **Proaktive Homepage-Dramaturgie:** Der User wird geführt: Problem verstehen, Lösung kennenlernen, Beweis sehen (Cases), Kontakt aufnehmen.
- **Tonalität:** Professionell aber menschlich, direkt ohne kalt zu sein. Österreichisch-europäisch, nicht amerikanisch-aufgedreht.
- **Keine Em-Dashes** in deutschem oder englischem Text. Komma, Doppelpunkt oder Satzumformung stattdessen.

---

## Phase 1: Analyse (JETZT STARTEN)

**Ziel dieser Phase:** Faktenbasierte Grundlage für alle späteren Entscheidungen. Keine Annahmen, keine Empfehlungen ohne Evidenz.

### 1.1 Aktuelle Website analysieren

URL: https://littlelights.studio

Analysiere folgende Punkte und erstelle einen strukturierten Report:

**Inhalt & Positionierung**
- Was kommuniziert die Homepage in den ersten 5 Sekunden?
- Welches Problem des Kunden wird adressiert (wenn überhaupt)?
- Wie werden die Leistungsbereiche dargestellt?
- Gibt es eine klare Hierarchie der Bereiche (Agency > Reels & Stories > Creative)?
- Wie werden Projekte/Case Studies präsentiert?
- Gibt es einen klaren Call to Action? Wo, wie oft, wie formuliert?

**Struktur & Navigation**
- Vollständige Seitenstruktur (alle verlinkten Seiten)
- Navigation: Was ist im Header, was im Footer?
- User Journey: Wie wird ein Erstbesucher durch die Seite geführt?
- Gibt es Seiten, die nirgends verlinkt sind (orphan pages)?

**Technisches**
- Ladezeit (subjektiv: schnell / langsam / sehr langsam)
- Funktionieren alle Videos?
- Mobile-Darstellung: offensichtliche Probleme?
- Sprachen: Wie ist die Zweisprachigkeit gelöst?

**Was fehlt offensichtlich**
- Fehlende Informationen, die ein potenzieller Kunde suchen würde
- Fehlende Conversion-Elemente
- Fehlende Trust-Signale

### 1.2 Konkurrenzanalyse

Analysiere folgende Websites nach demselben Schema und erstelle für jede eine kompakte Einschätzung:

- https://www.juhuufactory.com/
- https://touchevideoagentur.com/
- https://www.framefresh.com/
- https://www.henx.at/
- https://www.mountainmaster.at/
- https://www.soviso.at/about
- https://www.stilkraft-film.com/
- https://www.pulpmedia.at/

**Pro Konkurrent analysieren:**
- Positionierung: Wie beschreiben sie sich? Agentur, Produktionsfirma, Studio?
- Zielgruppe: Wen sprechen sie an? (Konzerne, KMUs, Agenturen?)
- Hauptnavigation und Seitenstruktur
- Wie werden Projekte/Cases gezeigt?
- Was ist ihr offensichtlicher Differenziator?
- Call to Action: Was soll der Besucher tun?
- Stärken der Website
- Schwächen / Lücken

**Synthese nach der Einzelanalyse:**
- Was macht fast jeder? (Branchenclichés, die wir vermeiden sollten)
- Wo sind Lücken, die Little Lights füllen kann?
- Welche Website ist am stärksten und warum?
- Welche Positionierungsfelder sind besetzt, welche nicht?

### 1.3 Marktpositionierungs-Map

Erstelle nach der Analyse eine einfache Positionierungsmatrix. Mögliche Achsen (Vorschlag, kann angepasst werden nach Analyseergebnis):
- X-Achse: Produktionsdienstleister vs. strategischer Partner
- Y-Achse: Großkunden/Konzerne vs. KMUs

Wo stehen die Konkurrenten? Wo steht Little Lights aktuell? Wo soll Little Lights stehen?

### 1.4 SEO-Basischeck (aktuelle Website)

- Werden relevante Begriffe in Titles und H1s verwendet? (z.B. "Imagefilm Wien", "Employer Branding Film", "Social Media Video Produktion Wien")
- Gibt es Meta Descriptions?
- Wie ist die URL-Struktur?
- Offensichtliche technische SEO-Probleme?

**Ziel-Keywords für Little Lights (Hypothese, zu validieren):**
- Imagefilm Wien / Imagefilm Agentur Wien
- Employer Branding Film / Employer Branding Video
- Brand Film Agentur Österreich
- Social Media Video Produktion Wien
- Reels Produktion Wien / Corporate Reels Wien

---

## Phase 2: Strategie & Konzept (NACH PHASE 1)

Erst starten, wenn Phase 1 besprochen und freigegeben ist.

### 2.1 Messaging-Architektur

Auf Basis der Analyseergebnisse:
- Übergeordnetes Positioning Statement für Little Lights (nicht ein Slogan, sondern eine klare interne Leitlinie)
- Messaging pro Bereich (Agency, Reels & Stories, Creative Studio)
- Jeweils: Problem des Kunden, unsere Antwort darauf, Beweis

### 2.2 Homepage-Dramaturgie

Detaillierter Aufbau der Homepage als Storytelling-Sequenz:
- Was sieht der User zuerst (Hero)?
- Welche Fragen beantwortet die Seite in welcher Reihenfolge?
- Wo und wie oft wird zum Kontakt aufgerufen?
- Welche Elemente bauen Vertrauen auf (Logos, Cases, Zahlen)?

### 2.3 Seitenarchitektur (final)

Ausgehend von der Ausgangshypothese in Abschnitt 4 und den Analyseergebnissen:
- Finale Seitenstruktur mit URLs
- Navigation (Header und Footer)
- Case-Study-Template-Felder
- Interne Verlinkungsstrategie

### 2.4 SEO-Strategie

- Finale Keyword-Zuordnung pro Seite
- Title-Tag- und Meta-Description-Konzept
- URL-Struktur
- Unterseiten-Strategie für Service-Seiten (Employer Branding, Imagefilm etc.) als SEO-Landingpages

---

## Phase 3: Build (NACH PHASE 2)

Erst starten, wenn Strategie und Seitenarchitektur besprochen und freigegeben sind.

### Was Claude Code baut

- Vollständige Website auf Basis der in Phase 2 definierten Struktur
- CMS-Integration (Art nach Empfehlung in Phase 2 entschieden)
- Case-Study-Template: selbstständig befüllbar durch Auftraggeber
- Zweisprachigkeit DE/EN (manuell gepflegte Texte)
- Video-Integration via Vimeo/YouTube (zuverlässig, formatflexibel)
- Kontaktformular
- Responsive Design
- SEO-Basisimplementierung
- Dark Background als Ausgangspunkt (Video-Content kommt auf dunklem Hintergrund gut zur Geltung; finale Entscheidung nach Phase 2)

### Was Claude Code NICHT baut (wird nachgeliefert)

- Finaler Copytext (wird separat erarbeitet)
- Case Studies (werden vom Auftraggeber eingetragen)
- Team-Fotos und Bios

---

## 6. Offene Punkte (vor Phase 2 zu klären)

- Finaler Name für den dritten Bereich (aktueller Arbeitstitel: Creative Studio)
- Entscheidung Calendly: ja oder nein
- Auswahl der initialen Case Studies für den Launch (3-5 pro Bereich empfohlen)
- Vorhandene CI-Materialien: Logo, Farben, Typo, Styleguide an Claude Code übergeben

---

## 7. Kontext für Claude Code: Wie der Auftraggeber denkt

Michael Sokolar (miso), CEO von Little Lights Studio, ist technisch versiert (Software Engineering Hintergrund), baut aktiv mit Claude Code und hat bereits zwei Websites damit erstellt. Er will keine Erklärungen für Selbstverständliches. Er will Empfehlungen, keine endlosen Optionslisten. Wenn etwas nicht gut ist, soll Claude Code das sagen. Tonalität in der Kommunikation: direkt, professionell, menschlich.

**Keine Em-Dashes** in deutschen oder englischen Texten. Komma, Doppelpunkt oder Satzumformung verwenden.
