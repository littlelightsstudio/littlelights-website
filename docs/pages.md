# Seitendatenbank
**Little Lights Studio | Export: 09.05.2026 | 19 Seiten**

Vollständiger Pages-Export für DE↔EN-Übersetzung + SEO/GEO-Pass.

**Workflow:**
1. Claude exportiert aus Payload → diese Datei
2. Inhalte/Übersetzungen werden inline gepflegt (`_(leer)_` durch EN ersetzen)
3. import-pages-from-md.py parst zurück und PATCHt Payload

**Konventionen:**
- Inline-Textänderung: direkt im Feld editieren
- Kommentar: Blockquote mit `>` (wird beim Re-Import ignoriert)
- `_(leer)_` Marker = Feld leer in DB. EN ersetzen, DE belassen wenn fehlt.
- Block-IDs in `(block-id: …)` sind die Identitäts-Anker — NICHT ändern.
- Felder im Format `_Lang-neutral: …_` sind nicht lokalisiert (Preise, IDs, Variants).

---

### 1. Über Uns

- **ID:** 20
- **URL-Path:** `/about`
- **Slug:** `about`
- **Area:** -
- **Visibility:** public

**Title DE:** Über Uns
**Title EN:** _(leer)_

#### Sections (5)

#### 1. `hero`
_(block-id: 69f605f7afb127458381bbf3)_

_Variant: editorial_

**Headline DE:** Unser Team
**Headline EN:** _(leer)_
**Subline DE:** Sieben Köpfe, ein Studio in Wien. Wir glauben, dass gute Filme aus echten Begegnungen entstehen.
**Subline EN:** _(leer)_
_Tag: Studio · Wien_

#### 2. `bold-statement`
_(block-id: 69f60643afb127458381bbf5)_

**Line 1 DE:** Wir machen keine Filme über Menschen.
**Line 1 EN:** _(leer)_
**Line 2 (Copper) DE:** Wir machen Filme mit ihnen.
**Line 2 (Copper) EN:** _(leer)_
**Tagline DE:** _(leer)_
**Tagline EN:** _(leer)_

#### 3. `magazine-manifest`
_(block-id: 69f60678afb127458381bbf7)_

**Eyebrow DE:** Anspruch
**Eyebrow EN:** _(leer)_
**Sub-Headline DE:** Wie wir arbeiten.
**Sub-Headline EN:** _(leer)_
**Lead DE:** Filme zu machen ist Handwerk. Filme, die wirken und ankommen, ist Beziehungsarbeit.
**Lead EN:** _(leer)_
**Body DE:**
> Drei Disziplinen, ein Anspruch. Wir entwickeln Brand-Filme, produzieren Reels & Stories für Social-First-Brands und arbeiten als Creative Studio an längeren Erzählformaten. Was die drei verbindet, ist die Frage, die wir uns am Anfang jedes Projekts stellen: Wofür stehst du?
> Diese Frage taucht in unseren Workshops auf, in den ersten Briefing-Calls und meistens noch einmal beim Set-Aufbau. Sie ist essentiell. Sie macht den Unterschied zwischen einem Film, der korrekt aussieht, und einem, an den Menschen sich erinnern.
> Wir glauben, dass gute Filme aus echten Begegnungen entstehen. Mit den Menschen vor der Kamera, mit den Auftraggebern, mit dem Team, das den Set aufbaut. Wenn das Klima stimmt, wird der Film besser. Punkt.
> Wir arbeiten am liebsten mit Marken, die das verstanden haben. Mit Agenturen, die uns als strategischen Partner sehen, nicht als Dienstleister. Mit Produkten und Geschichten, denen wir glauben können.

**Body EN:**
_(leer)_

##### Pull Quote
**Quote DE:** Wenn das Klima am Set stimmt, wird der Film besser.
**Quote EN:** _(leer)_

#### 4. `team-grid`
_(block-id: 69f607abafb127458381bbf9)_

**Headline DE:** Wer wir sind.
**Headline EN:** _(leer)_
**Subline DE:** _(leer)_
**Subline EN:** _(leer)_
_(Team-Mitglieder werden automatisch aus TeamMembers-Collection gezogen.)_

#### 5. `cta`
_(block-id: 69f607bfafb127458381bbfb)_

**Headline DE:** Lass uns reden.
**Headline EN:** Lass uns reden.
**Subline DE:** Wir freuen uns auf dein Projekt. Schreib uns ein paar Zeilen, wir melden uns spätestens am nächsten Werktag.
**Subline EN:** _(leer)_
_Variant: form_

---

#### SEO

**Meta Title DE:** _(leer)_
**Meta Title EN:** _(leer)_

**Meta Description DE:** _(leer)_
**Meta Description EN:** _(leer)_

---

### 2. AGB

- **ID:** 17
- **URL-Path:** `/agb`
- **Slug:** `agb`
- **Area:** -
- **Visibility:** public

**Title DE:** AGB
**Title EN:** _(leer)_

#### Sections (2)

#### 1. `hero`
_(block-id: 69f62422afb127458381bc05)_

_Variant: editorial_

**Headline DE:** AGB
**Headline EN:** _(leer)_
**Subline DE:** _(leer)_
**Subline EN:** _(leer)_
_Tag: Legal_

#### 2. `text-section`
_(block-id: 69f62438afb127458381bc07)_

**Eyebrow DE:** _(leer)_
**Eyebrow EN:** _(leer)_
**Headline DE:** _(leer)_
**Headline EN:** _(leer)_
**Content DE:**
## Geltungsbereich
Diese Allgemeinen Geschäftsbedingungen (AGB) gelten für alle Aufträge und Verträge zwischen der Little Lights Studio GmbH (im Folgenden "Studio") und ihren Kunden. Sie ergänzen und konkretisieren die Allgemeinen Herstellungs- und Lieferbedingungen des Fachverbands der Film- und Musikwirtschaft Österreichs (FAMA) für Auftrags- und Werbefilmproduktionen, Stand 1. Jänner 2026.
Soweit diese AGB Regelungen treffen, gehen sie den FAMA-Bedingungen vor. Im Übrigen gelten die FAMA-Bedingungen ergänzend.
Abweichende Bedingungen des Auftraggebers werden nur dann Vertragsbestandteil, wenn das Studio ihnen ausdrücklich schriftlich zustimmt.
## Feedback-Loops
In Abweichung von Punkt 3.11 der FAMA-Bedingungen sind im Rahmen einer Standard-Produktion pro Phase (Konzept, Offline-Schnitt, Online- und Final-Cut) jeweils 2 Feedback-Loops vorgesehen. Erst ab der dritten Korrekturschleife pro Phase werden zusätzliche Anpassungen gemäß Punkt 2.2 der FAMA-Bedingungen separat kalkuliert und vergütet.
Sonderwünsche wie zusätzliche Voiceover-Aufnahmen, Untertitelversionen oder Schnittfassungen für andere Formate sind hiervon nicht erfasst und werden separat verrechnet.
## Wettertage
In Ergänzung zu Punkt 2.2 der FAMA-Bedingungen gilt für wetterbedingte Drehabsagen Folgendes:
Wettertage sind Ersatz-Drehtage zu denselben Konditionen wie der ursprüngliche Drehtag, ohne zusätzliche Drehtags-Kosten.
Aufschläge entstehen durch:
- 50 Prozent Crew-Kompensation für den abgesagten Tag
- Zuschläge für Wochenenden, Feiertage oder kurzfristige Umplanung von Crew, Equipment oder Locations
- Zusatzkosten externer Dienstleister, die durch die Verschiebung entstehen
## Ergänzende Bestimmungen
In allen nicht oben geregelten Punkten gelten ausschließlich die Allgemeinen Herstellungs- und Lieferbedingungen des Fachverbands der Film- und Musikwirtschaft Österreichs (FAMA), Stand 1. Jänner 2026.
Stand: Mai 2026

**Content EN:**
_(leer)_

---

#### SEO

**Meta Title DE:** _(leer)_
**Meta Title EN:** _(leer)_

**Meta Description DE:** _(leer)_
**Meta Description EN:** _(leer)_

---

### 3. Agency

- **ID:** 4
- **URL-Path:** `/agency`
- **Slug:** `agency`
- **Area:** agency
- **Visibility:** public

**Title DE:** Agency
**Title EN:** _(leer)_

#### Sections (9)

#### 1. `hero`
_(block-id: 69f2f11c47d4aa108a1f46b2)_

_Variant: landing_

**Headline DE:** Agency
**Headline EN:** _(leer)_
**Subline DE:** _(leer)_
**Subline EN:** _(leer)_

#### 2. `bold-statement`
_(block-id: 69f3578a3de483b375ce8678)_

**Line 1 DE:** Filme, die strategisch
**Line 1 EN:** _(leer)_
**Line 2 (Copper) DE:** wirken.
**Line 2 (Copper) EN:** _(leer)_
**Tagline DE:** Employer Branding, das anzieht. Imagefilme, die positionieren. Kampagnen, die bleiben.
**Tagline EN:** _(leer)_

#### 3. `problem-statement`
_(block-id: 69f8953dafb127458381bc09)_

**Eyebrow DE:** Ehrlich gesagt.
**Eyebrow EN:** _(leer)_
**Headline DE:** Viele Unternehmensfilme funktionieren nicht.
**Headline EN:** _(leer)_
**Support Text DE:** Sie sind gut produziert, bleiben aber hübsche Bilder. Es fehlt am tragfähigen Storytelling, an Authentizität und an strategischer Grundlage.
**Support Text EN:** _(leer)_

#### 4. `magazine-manifest`
_(block-id: 69f897bfafb127458381bc0b)_

**Eyebrow DE:** Unsere Antwort.
**Eyebrow EN:** _(leer)_
**Sub-Headline DE:** _(leer)_
**Sub-Headline EN:** _(leer)_
**Lead DE:** Wir sind keine Filmproduktion, die Aufträge ausführt. Wir sind der Partner, der Kommunikation mitdenkt.
**Lead EN:** _(leer)_
**Body DE:**
Seit über zwölf Jahren arbeiten wir mit Unternehmen zusammen, die Film als strategisches Instrument verstehen. Diese Perspektive verändert alles - vom ersten Gespräch an.
Wir entwickeln Formate, die wachsen - auch wenn sie mit einem einzelnen Film beginnen. Wir bauen Archive auf, die über Jahre Wert schaffen, weil Geschichten nicht verfallen. Wir bauen Archive auf, die über Jahre Wert schaffen, weil Geschichten nicht verfallen. Und wir sorgen dafür, dass Menschen vor der Kamera echt wirken, im Doku-Moment wie in der inszenierten Szene: Authentizität ist für uns keine Frage des Formats, sondern der Haltung.
Wir arbeiten partnerschaftlich - auch gerne mit Werbeagenturen. Ohne Konkurrenz-Geste, ohne Eigen-Profilierung über Umwege. Unsere Aufgabe ist, dass am Ende der beste Film entsteht. Welcher Name auf dem Briefing steht, ist zweitrangig.
Storytelling vor Hochglanz. Authentizität vor Pose. Strategie vor Auftrag.

**Body EN:**
_(leer)_

##### Pull Quote
**Quote DE:** Gemeinsam wurden Formate entwickelt, die unsere Arbeitgebermarke konsistent und authentisch erlebbar machen.
**Quote EN:** _(leer)_
_Attribution: Michael Sagmeister, People & Culture Development Strabag_

#### 5. `services-grid`
_(block-id: 69f8a520821b3d24fbe757ea)_

**Eyebrow DE:** Unser Spektrum.
**Eyebrow EN:** _(leer)_
**Headline DE:** _(leer)_
**Headline EN:** _(leer)_
**Intro DE:** _(leer)_
**Intro EN:** _(leer)_

##### Service 1
**Eyebrow DE:** _(leer)_
**Eyebrow EN:** _(leer)_
**Title DE:** Employer Branding
**Title EN:** _(leer)_
**Description DE:** 150+ Karrierestories, Greiner Walks, EB-Imagefilme. Zwölf Jahre Spezialisierung auf authentische Arbeitgeberkommunikation, in der Serie wie im Einzelfilm.
**Description EN:** _(leer)_

##### Service 2
**Eyebrow DE:** _(leer)_
**Eyebrow EN:** _(leer)_
**Title DE:** Imagefilme
**Title EN:** _(leer)_
**Description DE:** Früher zeigten Imagefilme die teuren Maschinen. Wir zeigen die Werte des Unternehmens und das Problem, das es für seine Kunden löst.
**Description EN:** _(leer)_

##### Service 3
**Eyebrow DE:** _(leer)_
**Eyebrow EN:** _(leer)_
**Title DE:** Werbung & Kampagnen
**Title EN:** _(leer)_
**Description DE:** Emotionales Storytelling in Kurzform für TV, Streaming und Online. Wir produzieren eigenständig — und genauso gerne als Produktionspartner an der Seite einer Agentur.
**Description EN:** _(leer)_

##### Service 4
**Eyebrow DE:** _(leer)_
**Eyebrow EN:** _(leer)_
**Title DE:** Branded Entertainment
**Title EN:** _(leer)_
**Description DE:** Unterhaltungsformate mit Markenbezug. Geschichten, die wirken weil sie nicht als Werbung daherkommen.
**Description EN:** _(leer)_

##### Service 5
**Eyebrow DE:** _(leer)_
**Eyebrow EN:** _(leer)_
**Title DE:** Nachhaltigkeit
**Title EN:** _(leer)_
**Description DE:** Echte Stories, echte Menschen, echte Substanz. Glaubwürdigkeit entsteht durch zeigen, nicht durch behaupten.
**Description EN:** _(leer)_

##### Service 6
**Eyebrow DE:** _(leer)_
**Eyebrow EN:** _(leer)_
**Title DE:** Workshops & Keynotes
**Title EN:** _(leer)_
**Description DE:** Storytelling-Methodik aus 12 Jahren Praxis. Für Marketing-Teams, Konferenzen, interne Weiterbildung.
**Description EN:** _(leer)_

#### 6. `partnership-block`
_(block-id: 69f8acd2edaa3b45c2afbb5e)_

**Eyebrow DE:** Was Zusammenarbeit ergibt.
**Eyebrow EN:** _(leer)_
**Headline DE:** Tiefe entsteht über Zeit. In Beziehungen, in Formaten, in Performance.
**Headline EN:** _(leer)_

##### Pillar 1
**Eyebrow DE:** Partnerschaft.
**Eyebrow EN:** _(leer)_
**Headline DE:** Aus Auftrag wird Beziehung.
**Headline EN:** _(leer)_
**Body DE:**
_(leer)_

**Body EN:**
_(leer)_

##### Pillar 2
**Eyebrow DE:** Formatentwicklung
**Eyebrow EN:** _(leer)_
**Headline DE:** Wir entwickeln Eure Erzählform.
**Headline EN:** _(leer)_
**Body DE:**
_(leer)_

**Body EN:**
_(leer)_

##### Pillar 3
**Eyebrow DE:** Performance
**Eyebrow EN:** _(leer)_
**Headline DE:** Storytelling treibt Performance.
**Headline EN:** _(leer)_
**Body DE:**
_(leer)_

**Body EN:**
_(leer)_

#### 7. `projects-grid`
_(block-id: 69f8b4be15d86d7c3b15dd15)_

**Eyebrow DE:** Agentur-Projekte
**Eyebrow EN:** _(leer)_
**Big Headline DE:** Wo Filme
Wirkung zeigen.
**Big Headline EN:** _(leer)_
_Layout: grid · Aspect: landscape · Cols: 3_

#### 8. `testimonials`
_(block-id: 69f8b88c161c9929d14fc286)_

**Headline DE:** _(leer)_
**Headline EN:** _(leer)_
_Filter: area=agency · onlyFeatured=False_

#### 9. `cta`
_(block-id: 69f8b8a5161c9929d14fc288)_

**Headline DE:** Lass uns reden.
**Headline EN:** _(leer)_
**Subline DE:** _(leer)_
**Subline EN:** _(leer)_
_Variant: form_

---

#### SEO

**Meta Title DE:** _(leer)_
**Meta Title EN:** _(leer)_

**Meta Description DE:** _(leer)_
**Meta Description EN:** _(leer)_

---

### 4. Creative Studio

- **ID:** 6
- **URL-Path:** `/creative-studio`
- **Slug:** `creative-studio`
- **Area:** creative
- **Visibility:** public

**Title DE:** Creative Studio
**Title EN:** _(leer)_

#### Sections (7)

#### 1. `hero`
_(block-id: 69fcaf5a0862b1bb4e31be6d)_

_Variant: landing_

**Headline DE:** _(leer)_
**Headline EN:** _(leer)_
**Subline DE:** _(leer)_
**Subline EN:** _(leer)_

#### 2. `bold-statement`
_(block-id: 69fcaf840862b1bb4e31be6f)_

**Line 1 DE:** Geschichten,
**Line 1 EN:** _(leer)_
**Line 2 (Copper) DE:** die uns wach halten.
**Line 2 (Copper) EN:** _(leer)_
**Tagline DE:** Creative Studio
**Tagline EN:** _(leer)_

#### 3. `magazine-manifest`
_(block-id: 69fcafbe0862b1bb4e31be71)_

**Eyebrow DE:** Aus eigenem Antrieb.
**Eyebrow EN:** _(leer)_
**Sub-Headline DE:** _(leer)_
**Sub-Headline EN:** _(leer)_
**Lead DE:** Hier geht unsere kreative Kraft dorthin, wohin sie will.
**Lead EN:** _(leer)_
**Body DE:**
Was 2018 als Kurzgeschichte über Goblins begann, ist heute eine Fantasy-Trilogie. Zwei Bände sind erschienen, der dritte folgt zum Jahresende. Verlegt haben wir alles selbst. Little Lights Studio steht als offizieller Verlag in jedem Exemplar. Das war eine Studio-Entscheidung, kein Marketing.
Parallel produzieren wir Kurzfilme mit, entwickeln Dokumentarisches, reichen Stoffe in Förderung ein. Was hier wächst, wächst langsam, und das ist Absicht. Wir suchen Bücher und Filme, nicht Volumen.
Diese Arbeit hält uns wach. Sie hält die Erzählung scharf, auf der sonst der Produktionsalltag liegt. Und sie zieht Stoffe an. Manuskripte, Treatments, Anfragen von Menschen, die ein Studio erkennen, das lange Geschichten ernst nimmt. Was wir annehmen, lebt hier.

**Body EN:**
_(leer)_

##### Pull Quote
**Quote DE:** _(leer)_
**Quote EN:** _(leer)_

#### 4. `dual-path`
_(block-id: 69fcb02d0862b1bb4e31be73)_

**Section Eyebrow DE:** Zwei Richtungen.
**Section Eyebrow EN:** _(leer)_
**Section Headline DE:** Unsere Kreativprojekte
**Section Headline EN:** _(leer)_
**Section Intro DE:** _(leer)_
**Section Intro EN:** _(leer)_

##### Path 1
**Eyebrow DE:** _(leer)_
**Eyebrow EN:** _(leer)_
**Headline DE:** Kurz- & Langfilme
**Headline EN:** _(leer)_
**Body DE:**
Wir entwickeln eigene Stoffe, schreiben mit, ko-produzieren. Aktuell läuft ein Kurzfilm in Ko-Produktion, dazu Dokumentarfilme in der Entwicklung. Was hier entsteht, hat Zeit.
Unser Slate

**Body EN:**
_(leer)_

##### Path 2
**Eyebrow DE:** _(leer)_
**Eyebrow EN:** _(leer)_
**Headline DE:** Little Lights Verlag
**Headline EN:** _(leer)_
**Body DE:**
Wir verlegen offiziell als Little Lights Studio. Aktuell  die Helena Flinn Chronicles, eine Middle-Grade-Fantasy-Trilogie, plus die wachsende Storyworld auf helenaflinn.com. Wir kuratieren, statt zu skalieren. Wenn ein Manuskript zu uns passt, machen wir Platz.
Zur Verlags-Seite

**Body EN:**
_(leer)_

##### Pull Quote
**Quote DE:** Der Antrieb ist derselbe. 
Herzensprojekte denen wir helfen das Licht der Welt zu erblicken.
**Quote EN:** _(leer)_

#### 5. `projects-grid`
_(block-id: 69fcb0c40862b1bb4e31be79)_

**Eyebrow DE:** Aus eigener Kraft.
**Eyebrow EN:** _(leer)_
**Big Headline DE:** Little Lights Projekte.
**Big Headline EN:** _(leer)_
_Layout: grid · Aspect: landscape · Cols: 2_

#### 6. `testimonials`
_(block-id: 69fcb11d0862b1bb4e31be7b)_

**Headline DE:** _(leer)_
**Headline EN:** _(leer)_
_Filter: area=creative · onlyFeatured=True_

#### 7. `cta`
_(block-id: 69fcb1390862b1bb4e31be7d)_

**Headline DE:** Lass uns quatschen.
**Headline EN:** _(leer)_
**Subline DE:** Habt ihr einen Stoff? Oder habt ihr Fragen? Schreibt uns!
**Subline EN:** _(leer)_
_Variant: form_

---

#### SEO

**Meta Title DE:** _(leer)_
**Meta Title EN:** _(leer)_

**Meta Description DE:** _(leer)_
**Meta Description EN:** _(leer)_

---

### 5. Datenschutz

- **ID:** 18
- **URL-Path:** `/datenschutz`
- **Slug:** `datenschutz`
- **Area:** -
- **Visibility:** public

**Title DE:** Datenschutz
**Title EN:** _(leer)_

#### Sections (2)

#### 1. `hero`
_(block-id: 69f61f74afb127458381bbfd)_

_Variant: editorial_

**Headline DE:** Datenschutz
**Headline EN:** _(leer)_
**Subline DE:** _(leer)_
**Subline EN:** _(leer)_
_Tag: Legal_

#### 2. `text-section`
_(block-id: 69f62024afb127458381bbff)_

**Eyebrow DE:** _(leer)_
**Eyebrow EN:** _(leer)_
**Headline DE:** _(leer)_
**Headline EN:** _(leer)_
**Content DE:**
## Verantwortlicher
Little Lights Studio GmbH, Lange Gasse 72/5, 1080 Wien.
E-Mail: 
Telefon: +43 676 361 86 08
## Allgemeines
Wir behandeln deine personenbezogenen Daten vertraulich und entsprechend der gesetzlichen Datenschutzvorschriften (DSGVO, DSG 2018, TMG). Diese Erklärung beschreibt, welche Daten wir erfassen, wofür wir sie verarbeiten, und welche Rechte du hast.
## Hosting
Unsere Website wird auf Servern der Hetzner Online GmbH (Industriestr. 25, 91710 Gunzenhausen, Deutschland) in der EU gehostet. Mit Hetzner besteht ein Auftragsverarbeitungsvertrag (AVV) gemäß Art. 28 DSGVO. Rechtsgrundlage: Art. 6 Abs. 1 lit. f DSGVO (berechtigtes Interesse an stabiler Bereitstellung).
## Server-Logfiles
Bei jedem Aufruf der Website werden automatisch übermittelte Daten erfasst (IP-Adresse, Datum und Uhrzeit, Browser-Typ, aufgerufene Seite, Referrer). Die Speicherung erfolgt für maximal 14 Tage zur Sicherstellung des Betriebs und Abwehr missbräuchlicher Zugriffe (Art. 6 Abs. 1 lit. f DSGVO).
## Webanalyse mit Umami
Wir verwenden Umami, eine selbst gehostete und datenschutzfreundliche Webanalyse. Umami arbeitet ohne Cookies, anonymisiert IP-Adressen, und speichert keine personenbezogenen Daten. Es werden lediglich aggregierte Statistiken erhoben (Seitenaufrufe, Verweildauer, Browser, Land). Eine Einwilligung ist daher nicht erforderlich. Rechtsgrundlage: Art. 6 Abs. 1 lit. f DSGVO (berechtigtes Interesse an der Verbesserung unseres Angebots).
## Schriften
Die verwendeten Schriften Satoshi und Clash Display (Indian Type Foundry, Lizenz: Fontshare) werden direkt von unserem Server ausgeliefert. Es findet keine Übermittlung von Daten an Drittanbieter statt.
## Videos (Bunny.net)
Hintergrund-Videos werden über Bunny.net (BunnyWay d.o.o., Slowenien, EU) eingebunden. Im Standard-Modus verwendet Bunny.net keine Tracking-Cookies. Beim Abspielen wird deine IP-Adresse an Bunny.net übermittelt. Rechtsgrundlage: Art. 6 Abs. 1 lit. f DSGVO.
## Newsletter (MailerLite)
Für unseren Newsletter nutzen wir MailerLite (UAB MailerLite, Litauen, EU). Bei der Anmeldung verarbeiten wir deine E-Mail-Adresse und gegebenenfalls Vor- und Nachname. Rechtsgrundlage: Einwilligung (Art. 6 Abs. 1 lit. a DSGVO). Wir messen Öffnungs- und Klickraten zur Verbesserung der Newsletter-Inhalte. Du kannst deine Einwilligung jederzeit widerrufen. Der Abmelde-Link befindet sich in jeder Newsletter-Mail.
## E-Mail (Google Workspace)
Geschäftliche Kommunikation läuft über Google Workspace (Google Ireland Limited, Irland, EU). Bei E-Mail-Korrespondenz verarbeiten wir die übermittelten Inhalte zur Beantwortung deiner Anfrage. Rechtsgrundlage: Art. 6 Abs. 1 lit. f DSGVO.
## Kommunikation und Kollaboration
Im Rahmen von Projekt-Kollaboration nutzen wir bedarfsweise Microsoft Teams, Zoom, Google Drive und OneDrive. Die jeweiligen Anbieter verarbeiten Daten gemäß ihrer eigenen Datenschutzerklärungen. Mit allen externen Anbietern bestehen Auftragsverarbeitungsverträge gemäß Art. 28 DSGVO.
## Cookies
Unsere Website setzt keine Tracking- oder Marketing-Cookies. Technisch erforderliche Cookies (z.B. für Sitzungsverwaltung) werden auf Basis Art. 6 Abs. 1 lit. f DSGVO gesetzt. Eine Einwilligung ist hierfür nicht erforderlich.
## SSL- und TLS-Verschlüsselung
Aus Sicherheitsgründen und zum Schutz vertraulicher Inhalte nutzen wir SSL- bzw. TLS-Verschlüsselung. Eine verschlüsselte Verbindung erkennst du am https-Präfix in der Adressleiste deines Browsers.
## Einsatz von KI-Werkzeugen
Wir setzen Werkzeuge der Künstlichen Intelligenz (KI) für unsere kreative und technische Arbeit ein. Soweit dabei personenbezogene Daten verarbeitet werden, informieren wir Sie nachstehend transparent über die eingesetzten Anbieter, Zwecke und Datenflüsse.
### Eingesetzte KI-Anbieter
Anthropic Claude (Anthropic, PBC, San Francisco, USA)
Wir nutzen Claude in verschiedenen Formen (Chat, Code, integrierte Workflows) für interne Recherche, Code-Entwicklung und Konzeptionsarbeit. In aller Regel werden hierbei keine personenbezogenen Daten verarbeitet. Falls ausnahmsweise personenbezogene Daten betroffen sind, geschieht dies nur über vertragliche Konfigurationen, die keine Trainingsdaten-Verwendung zulassen. Datenübermittlung in die USA auf Basis der EU-Standardvertragsklauseln (SCC) und ergänzender Schutzmaßnahmen. Weiterführende Informationen: https://www.anthropic.com/privacy.
ElevenLabs (ElevenLabs Inc., New York, USA)
Selektive Nutzung für Audio-Synthese und Voice-Generierung in Produktionen. Verarbeitete Daten: Sprachsamples und Skripttexte. Bei Verwendung von Stimmen realer Personen ausschließlich auf Basis ausdrücklicher schriftlicher Einwilligung der betroffenen Person. Datenübermittlung in die USA auf Basis der EU-Standardvertragsklauseln. Weiterführende Informationen: https://elevenlabs.io/privacy.
Generative KI für Bild- und Video-Inhalte (variierende Anbieter)
Im Rahmen von Konzept-Visualisierungen und Pitches setzen wir generative KI-Werkzeuge ein. In der Regel werden hierbei keine personenbezogenen Daten verarbeitet. Eine aktuelle Übersicht der eingesetzten Anbieter halten wir intern im KI-Inventar nach.
Adobe Creative Cloud inkl. Adobe Firefly (Adobe Inc., USA)
Standard-Postproduktionssoftware mit integrierten KI-Funktionen. Adobe ist nach dem EU-US Data Privacy Framework zertifiziert. Wir haben Trainingsdaten-Nutzung für Cloud-synchronisierte Inhalte deaktiviert. Weiterführende Informationen: https://www.adobe.com/privacy.html.
### Zwecke
- Entwicklungs- und Recherche-Unterstützung in Konzeption und Skripting
- Postproduktion und Audio-/Video-Bearbeitung
- Visuelle Konzept-Entwicklung in Pitches und Präsentationen
- Selektive Verwendung in finalen Produktionen, jeweils mit ausdrücklicher Kundenfreigabe und Kennzeichnung gegenüber dem Endpublikum
### Rechtsgrundlage
Die Verarbeitung erfolgt auf Grundlage von Art. 6 Abs. 1 lit. b DSGVO (Vertragsdurchführung mit Auftraggebern) und Art. 6 Abs. 1 lit. f DSGVO (berechtigtes Interesse an effizienter und qualitativ hochwertiger Leistungserbringung). Bei Verarbeitung biometrischer Daten (Stimm- oder Gesichts-Samples realer Personen) ausschließlich auf Grundlage ausdrücklicher Einwilligung gemäß Art. 9 Abs. 2 lit. a DSGVO.
### Drittlandübermittlung
Die genannten Anbieter haben ihren Sitz teilweise in den USA. Übermittlung erfolgt auf Basis der EU-Standardvertragsklauseln (SCC) gemäß Art. 46 Abs. 2 lit. c DSGVO. Adobe ist zusätzlich nach dem EU-US Data Privacy Framework zertifiziert.
### Speicherdauer
Eingaben und Ergebnisse werden bei den Anbietern gemäß deren jeweiligen Aufbewahrungsfristen gespeichert. Wir selbst speichern projektbezogene KI-Ergebnisse nur so lange, wie für die Vertragsdurchführung und gesetzliche Aufbewahrungspflichten erforderlich.
### Kennzeichnung KI-generierter Inhalte
Soweit wir in finalen Werken substantiell KI-generierte oder KI-manipulierte Inhalte einsetzen, kennzeichnen wir diese gemäß Art. 50 EU AI Act gegenüber dem Publikum. Eine projektbezogene Kennzeichnung finden Sie auf der jeweiligen Projektseite unserer Website.
## Deine Rechte
Du hast folgende Rechte gegenüber uns:
- Auskunft über deine gespeicherten Daten (Art. 15 DSGVO)
- Berichtigung unrichtiger Daten (Art. 16 DSGVO)
- Löschung (Art. 17 DSGVO)
- Einschränkung der Verarbeitung (Art. 18 DSGVO)
- Datenübertragbarkeit (Art. 20 DSGVO)
- Widerspruch gegen Verarbeitungen auf Basis berechtigten Interesses (Art. 21 DSGVO)
- Widerruf erteilter Einwilligungen (Art. 7 Abs. 3 DSGVO)
- Beschwerde bei der Aufsichtsbehörde
Beschwerde bei der österreichischen Datenschutzbehörde, Barichgasse 40-42, 1030 Wien, . Anfragen an uns bitte per E-Mail an .
## Datenübermittlung in Drittländer
Soweit personenbezogene Daten an Anbieter außerhalb der EU oder des EWR übermittelt werden, geschieht dies auf Basis der Standardvertragsklauseln (SCC) der Europäischen Kommission und mit zusätzlichen Garantien gemäß DSGVO.
Stand: Mai 2026

**Content EN:**
_(leer)_

---

#### SEO

**Meta Title DE:** _(leer)_
**Meta Title EN:** _(leer)_

**Meta Description DE:** _(leer)_
**Meta Description EN:** _(leer)_

---

### 6. Homepage

- **ID:** 3
- **URL-Path:** `/home`
- **Slug:** `home`
- **Area:** -
- **Visibility:** public

**Title DE:** Homepage
**Title EN:** _(leer)_

#### Sections (8)

#### 1. `hero`
_(block-id: 69df933442750aa182929c0b)_

_Variant: full_

**Headline DE:** Filme, die ankommen.
**Headline EN:** _(leer)_
**Subline DE:** Strategische Filmproduktion für Unternehmen, die Bewegtbild als Kommunikationsinstrument verstehen.
**Subline EN:** _(leer)_
_Tag: Brand Film Agentur Wien_

#### 2. `bold-statement`
_(block-id: 69df933442750aa182929c0c)_

**Line 1 DE:** Jeder behauptet Storytelling.
**Line 1 EN:** _(leer)_
**Line 2 (Copper) DE:** Wir leben es.
**Line 2 (Copper) EN:** _(leer)_
**Tagline DE:** Drei Disziplinen. Eine Handschrift.
**Tagline EN:** _(leer)_

#### 3. `diagonal-slider`
_(block-id: 69df933442750aa182929c10)_

##### Panel 1
_Label (Copper, lang-neutral): Agency_
**Headline DE:** Filme, die strategisch wirken.
**Headline EN:** _(leer)_
**Body DE:** Imagefilme. Employer Branding. Werbespots.
**Body EN:** _(leer)_
**Body (Hover) DE:** Langfristige Partnerschaften statt Einzelprojekte.
**Body (Hover) EN:** _(leer)_
**Link Label DE:** Mehr erfahren
**Link Label EN:** _(leer)_

##### Panel 2
_Label (Copper, lang-neutral): Reels & Stories_
**Headline DE:** Formate, die funktionieren.
**Headline EN:** _(leer)_
**Body DE:** Social Media Content mit Plan.
**Body EN:** _(leer)_
**Body (Hover) DE:** Alles beginn mit einem Workshop.
**Body (Hover) EN:** _(leer)_
**Link Label DE:** Mehr erfahren
**Link Label EN:** _(leer)_

##### Panel 3
_Label (Copper, lang-neutral): Creative Studio_
**Headline DE:** Our Stories
**Headline EN:** _(leer)_
**Body DE:** Bücher, Kurzfilme, Dokumentarfilme.
**Body EN:** _(leer)_
**Body (Hover) DE:** Projekte, die aus eigener Initiative entstehen.
**Body (Hover) EN:** _(leer)_
**Link Label DE:** Entdecken
**Link Label EN:** _(leer)_


#### 4. `projects-grid`
_(block-id: 69df933442750aa182929c11)_

**Eyebrow DE:** Ausgewählte Arbeiten
**Eyebrow EN:** _(leer)_
**Big Headline DE:** Projekte, die zeigen\nwas wir meinen.
**Big Headline EN:** _(leer)_
_Layout: pyramid · Aspect: landscape · Cols: 3_

#### 5. `client-logos`
_(block-id: 69df933442750aa182929c18)_

_(Client logos: 5 entries — no localized text.)_

#### 6. `stats`
_(block-id: 69df933442750aa182929c19)_

**Headline DE:** Kein Projekt.
**Headline EN:** _(leer)_
**Headline Accent DE:** Eine Partnerschaft.
**Headline Accent EN:** _(leer)_

##### Stat 1
_Number: 12+_
**Label DE:** Jahre
**Label EN:** _(leer)_

##### Stat 2
_Number: 600+_
**Label DE:** Filmprojekte
**Label EN:** _(leer)_

##### Stat 3
_Number: 50+_
**Label DE:** Kunden
**Label EN:** _(leer)_

##### Stat 4
_Number: 7_
**Label DE:** Filmemacher
**Label EN:** _(leer)_

#### 7. `testimonials`
_(block-id: 69df933442750aa182929c1a)_

**Headline DE:** Was unsere Partner sagen
**Headline EN:** _(leer)_
_Filter: area=all · onlyFeatured=True_

#### 8. `cta`
_(block-id: 69df933442750aa182929c1b)_

**Headline DE:** Lass uns reden.
**Headline EN:** _(leer)_
**Subline DE:** Kein Pitch. Nur ein ehrliches Kennenlernen.
**Subline EN:** _(leer)_
_Variant: form_

---

#### SEO

**Meta Title DE:** _(leer)_
**Meta Title EN:** _(leer)_

**Meta Description DE:** _(leer)_
**Meta Description EN:** _(leer)_

---

### 7. Impressum

- **ID:** 19
- **URL-Path:** `/impressum`
- **Slug:** `impressum`
- **Area:** -
- **Visibility:** public

**Title DE:** Impressum
**Title EN:** _(leer)_

#### Sections (2)

#### 1. `hero`
_(block-id: 69f62336afb127458381bc01)_

_Variant: editorial_

**Headline DE:** Impressum
**Headline EN:** _(leer)_
**Subline DE:** _(leer)_
**Subline EN:** _(leer)_
_Tag: Legal_

#### 2. `text-section`
_(block-id: 69f6234aafb127458381bc03)_

**Eyebrow DE:** _(leer)_
**Eyebrow EN:** _(leer)_
**Headline DE:** _(leer)_
**Headline EN:** _(leer)_
**Content DE:**
## Medieninhaber & Diensteanbieter
Little Lights Studio GmbH
Lange Gasse 72/5, 1080 Wien
Österreich
E-Mail: 
Telefon: +43 676 361 86 08
## Geschäftsführung
Michael Sokolar
## Firmenbuch & Behörden
Firmenbuchnummer: FN 414354 w
Firmenbuchgericht: Handelsgericht Wien
UID-Nummer: ATU68586648
Gewerberechtliche Vorschriften: Gewerbeordnung 1994 (www.ris.bka.gv.at)
Aufsichtsbehörde: Magistratisches Bezirksamt für den 8. Bezirk, Wien
Mitglied: Wirtschaftskammer Wien, Fachvertretung Film- und Musikindustrie
## Unternehmensgegenstand
Filmproduktion, Brand Storytelling, Creative Studio.
## Verantwortlich für den Inhalt
Michael Sokolar (Anschrift wie oben)
## Online-Streitbeilegung
Die Europäische Kommission stellt eine Plattform zur Online-Streitbeilegung (OS) bereit: ec.europa.eu/consumers/odr.
## Haftungsausschluss
Die Inhalte dieser Website wurden mit größter Sorgfalt erstellt. Für die Richtigkeit, Vollständigkeit und Aktualität der Inhalte können wir keine Gewähr übernehmen. Für externe Links übernehmen wir trotz sorgfältiger Kontrolle keine Haftung. Für die Inhalte verlinkter Seiten ist ausschließlich deren Betreiber verantwortlich.
## Urheberrecht
Sämtliche Inhalte dieser Website unterliegen dem österreichischen Urheberrecht. Vervielfältigung, Bearbeitung, Verbreitung oder Verwertung außerhalb der Grenzen des Urheberrechts erfordert die schriftliche Zustimmung der Little Lights Studio GmbH.
Stand: Mai 2026

**Content EN:**
_(leer)_

---

#### SEO

**Meta Title DE:** _(leer)_
**Meta Title EN:** _(leer)_

**Meta Description DE:** _(leer)_
**Meta Description EN:** _(leer)_

---

### 8. Reels & Stories

- **ID:** 5
- **URL-Path:** `/reels-stories`
- **Slug:** `reels-stories`
- **Area:** rs
- **Visibility:** public

**Title DE:** Reels & Stories
**Title EN:** _(leer)_

#### Sections (12)

#### 1. `hero`
_(block-id: 69fb36049b538300f9b93eae)_

_Variant: landing_

**Headline DE:** _(leer)_
**Headline EN:** _(leer)_
**Subline DE:** _(leer)_
**Subline EN:** _(leer)_

#### 2. `bold-statement`
_(block-id: 69fb3e499b538300f9b93eb0)_

**Line 1 DE:** Drauflos drehen
**Line 1 EN:** _(leer)_
**Line 2 (Copper) DE:** kannst du selbst.
**Line 2 (Copper) EN:** _(leer)_
**Tagline DE:** Reels & Stories
**Tagline EN:** _(leer)_

#### 3. `problem-statement`
_(block-id: 69fb3e629b538300f9b93eb2)_

**Eyebrow DE:** Die Lage.
**Eyebrow EN:** _(leer)_
**Headline DE:** Social Media Content kann inzwischen jeder produzieren. Strategisches Storytelling können wenige liefern.
**Headline EN:** _(leer)_
**Support Text DE:** Die Plattformen sind voll mit Bewegtbild. Was selten ist, ist die Verbindung aus filmischer Qualität, klarer Markenführung und einer Methode, die über das einzelne Reel hinausreicht.
**Support Text EN:** _(leer)_

#### 4. `magazine-manifest`
_(block-id: 69fb3ea09b538300f9b93eb4)_

**Eyebrow DE:** Unsere Antwort.
**Eyebrow EN:** _(leer)_
**Sub-Headline DE:** _(leer)_
**Sub-Headline EN:** _(leer)_
**Lead DE:** Alles startet mit einem Workshop.
**Lead EN:** _(leer)_
**Body DE:**
Wir machen seit über zwölf Jahren Filme für große Marken. Strabag, Greiner, Volksbank oder Austria Tourism. Was wir dort gelernt haben, fließt jetzt in ein Produkt für kleinere Unternehmen ein. Reels und Stories, gebaut wie eine Markenkampagne. Mit einem narrativen Kern, einer eigenen Form und einer Logik, die euch trägt, statt euch zu zwingen, jeden Monat einen neuen Trend zu kopieren.
Bevor wir filmen, klären wir das Wichtigste: Wofür stehen wir? Wen sprechen wir an? Welche Geschichten erzählen nur wir? Diese Antworten sind die Grundlage für alles, was danach passiert. Ohne sie ist jedes Reel nur ein weiteres Reel im Feed.
In einem halbtägigen Workshop entsteht eure Content-Architektur. Drei Säulen, neun Formate, klare Zielgruppen. Aus diesem Fundament leiten sich alle künftigen Drehs ab, und ihr bekommt einen Storytelling Guide als Dokument, der so konkret ist, dass auch externe Partner damit arbeiten können.
Was uns von vielen Angeboten am Markt unterscheidet: Wir trennen Storytelling-Konzept und filmische Umsetzung nicht. Was woanders zwei separate Workflows sind, ist bei uns eine Disziplin. Gewachsen aus zwölf Jahren Markenfilmarbeit, runtergebrochen auf ein Format, das auch für kleinere Unternehmen wirtschaftlich Sinn ergibt.
Mehr zum Workshop

**Body EN:**
_(leer)_

##### Pull Quote
**Quote DE:** Was mich am meisten überrascht hat, war die Wirkung der Reels: deutlich mehr Sichtbarkeit, spürbar höhere Reichweite und ein viel professionellerer Auftritt nach außen. Ergebnisse, die wirklich etwas bewegen.
**Quote EN:** _(leer)_
_Attribution: Christoph Masin, Chief Tea Officer, JägerTEE_

#### 5. `partnership-block`
_(block-id: 69fb3f059b538300f9b93eb6)_

**Eyebrow DE:** Was im Workshop entsteht.
**Eyebrow EN:** _(leer)_
**Headline DE:** Drei Säulen. Neun Formate. Eine Methode.
**Headline EN:** _(leer)_

##### Pillar 1
**Eyebrow DE:** Säule 01 · Identifikation
**Eyebrow EN:** _(leer)_
**Headline DE:** Wer ihr seid
**Headline EN:** _(leer)_
**Body DE:**
_(leer)_

**Body EN:**
_(leer)_

##### Pillar 2
**Eyebrow DE:** Säule 02 · Expertise
**Eyebrow EN:** _(leer)_
**Headline DE:** Was ihr wisst
**Headline EN:** _(leer)_
**Body DE:**
_(leer)_

**Body EN:**
_(leer)_

##### Pillar 3
**Eyebrow DE:** Säule 03 · Beweis
**Eyebrow EN:** _(leer)_
**Headline DE:** Was ihr macht
**Headline EN:** _(leer)_
**Body DE:**
_(leer)_

**Body EN:**
_(leer)_

#### 6. `magazine-manifest`
_(block-id: 69fb3f779b538300f9b93ebe)_

**Eyebrow DE:** Wie es weitergeht.
**Eyebrow EN:** _(leer)_
**Sub-Headline DE:** _(leer)_
**Sub-Headline EN:** _(leer)_
**Lead DE:** Nach dem Workshop entscheidet ihr.
**Lead EN:** _(leer)_
**Body DE:**
Der Workshop liefert das Fundament. Was danach kommt, hängt von eurer Realität ab. Wir haben absichtlich kein One-Size-Paket gebaut. Stattdessen drei modulare Konstellationen, die wir mit euch zusammensetzen, je nachdem, was ihr schon habt.
Wenn ihr selbst dreht oder einen Videograph habt, übernehmen wir Konzept und Schnitt. Wenn ihr alles aus einer Hand wollt, übernehmen wir die komplette Produktion samt Posting. Wenn ihr eine Social-Media-Agentur an Bord habt, ergänzen wir um Storytelling-Expertise und filmische Premium-Produktionen, ohne ihr ins Handwerk zu pfuschen.
Wir konkurrieren nicht mit eurer bestehenden Struktur. Wir füllen die Lücke, die die meisten Strukturen haben: die Verbindung aus Strategie, Story und Bild.
Mehr zur Content Produktion

**Body EN:**
_(leer)_

##### Pull Quote
**Quote DE:** _(leer)_
**Quote EN:** _(leer)_

#### 7. `services-grid`
_(block-id: 69fb41dfc5ee5d4dd4325cc2)_

**Eyebrow DE:** So arbeiten wir mit euch.
**Eyebrow EN:** _(leer)_
**Headline DE:** Wir schneidern, statt zu verkaufen.
**Headline EN:** _(leer)_
**Intro DE:** Drei typische Konstellationen, plus alles dazwischen. Wir mischen die Bausteine so, dass das Setup zu eurer Realität passt.
**Intro EN:** _(leer)_

##### Service 1
**Eyebrow DE:** Selbst drehen.
**Eyebrow EN:** _(leer)_
**Title DE:** Plan und Schnitt von uns
**Title EN:** _(leer)_
**Description DE:** Ihr habt einen Videograph oder dreht selbst. Wir liefern monatlich Drehpläne mit Scripts und Shot-Listen und übernehmen Schnitt und Finishing.
**Description EN:** _(leer)_

##### Service 2
**Eyebrow DE:** Aus einer Hand.
**Eyebrow EN:** _(leer)_
**Title DE:** Wir planen & produzieren
**Title EN:** _(leer)_
**Description DE:** Konzeption, Drehtag, Postproduction, Postings. Vom monatlichen Planungsgespräch bis zur Veröffentlichung über euer Tool.
**Description EN:** _(leer)_

##### Service 3
**Eyebrow DE:** Mit eurer Agentur.
**Eyebrow EN:** _(leer)_
**Title DE:** Storytelling und Premium-Produktion
**Title EN:** _(leer)_
**Description DE:** Ihr habt eine Social-Media-Agentur. Wir bringen die Storytelling-Strategie und die filmische Tiefe für Premium-Formate, ohne ihrer Ausspielung ins Handwerk zu pfuschen.
**Description EN:** _(leer)_

##### Service 4
**Eyebrow DE:** Etwas dazwischen.
**Eyebrow EN:** _(leer)_
**Title DE:** Wir setzen es zusammen
**Title EN:** _(leer)_
**Description DE:** Eure Realität passt nicht in eine der drei Konstellationen? Erzählt uns davon. Wir kombinieren die Bausteine so, wie es zu eurer Struktur, eurem Budget und euren Zielen passt.
**Description EN:** _(leer)_

#### 8. `projects-grid`
_(block-id: 69fb43a0c5ee5d4dd4325cce)_

**Eyebrow DE:** Ausgewählte Arbeiten.
**Eyebrow EN:** _(leer)_
**Big Headline DE:** Reels mit Strategie.
Stories mit Substanz.
**Big Headline EN:** _(leer)_
_Layout: grid · Aspect: portrait · Cols: 4_

#### 9. `text-section`
_(block-id: 69fb431ec5ee5d4dd4325ccc)_

**Eyebrow DE:** Was es kostet.
**Eyebrow EN:** _(leer)_
**Headline DE:** Modular gerechnet. Nicht im Paket gepresst.
**Headline EN:** _(leer)_
**Content DE:**
Wir verkaufen kein Standard-Abo, das ihr ausfüllen müsst. Wir setzen euer Setup aus drei Bausteinen zusammen: Workshop, Produktion, Betreuung. Welche davon ihr braucht und in welchem Volumen, klären wir im Erstgespräch.
Der Workshop ist der Eintritt. Aktuell ab 950 €, einmalig. Wir halten den Einstiegspreis bewusst zugänglich, damit auch ein kleineres Unternehmen diesen Schritt gehen kann.
Die laufende Produktion startet ab 550 € pro Monat für reine Konzeption und Drehplanung und skaliert über Drehtage, Postproduction und Social-Media-Betreuung nach Bedarf. Vollständige Setups bewegen sich zwischen 2.500€ und 4.500€ pro Monat- mit monatlichem Drehtag, Schnitt und Posting. Längere Laufzeiten kommen mit Rabatten von bis zu 20 %.
Genaue Konfiguration und Pricing klären wir persönlich - wenn wir wissen, was ihr braucht.

**Content EN:**
_(leer)_

#### 10. `testimonials`
_(block-id: 69fb43cdc5ee5d4dd4325cd0)_

**Headline DE:** _(leer)_
**Headline EN:** _(leer)_
_Filter: area=rs · onlyFeatured=False_

#### 11. `faq`
_(block-id: 69fb43f7c5ee5d4dd4325cd4)_

**Eyebrow DE:** Klartext.
**Eyebrow EN:** _(leer)_
**Headline DE:** Was uns oft gefragt wird.
**Headline EN:** _(leer)_

##### FAQ 1
**Question DE:** Was kostet ein Workshop?
**Question EN:** _(leer)_
**Answer DE:**
Aktuell ab 950 €, einmalig. Im Workshop entsteht eure Content-Architektur: narrativer Kern, drei Säulen, neun Formate, ein Storytelling Guide als Dokument. Diese Investition wirkt monatelang, weil ihr danach nicht mehr bei jedem Dreh die Strategie neu erfinden müsst. Wir halten den Einstieg bewusst zugänglich, damit der Schritt für ein KMU machbar ist.

**Answer EN:**
_(leer)_

##### FAQ 2
**Question DE:** Wir haben schon einen Videograph oder eine Social-Media-Agentur. Passt das?
**Question EN:** _(leer)_
**Answer DE:**
Ja, das ist sogar oft der Idealfall. Bei einem internen Videograph übernehmen wir Plan und Schnitt: ihr dreht weiter, wir liefern Konzept, Scripts und Postproduction. Bei einer Social-Media-Agentur ergänzen wir um Storytelling-Tiefe und Premium-Produktion, ohne ihrer Ausspielung ins Handwerk zu pfuschen. Wir konkurrieren nicht, wir füllen die Lücke.

**Answer EN:**
_(leer)_

##### FAQ 3
**Question DE:** Wie schnell startet die Produktion?
**Question EN:** _(leer)_
**Answer DE:**
Workshop und erstes Konzept innerhalb von zwei bis vier Wochen. Erster Drehtag meist im Folgemonat. Sobald das Fundament steht, läuft alles in monatlichen Zyklen: Planungscall, Drehtag, Postings.

**Answer EN:**
_(leer)_

##### FAQ 4
**Question DE:** Welche Plattformen bedient ihr?
**Question EN:** _(leer)_
**Answer DE:**
Kurz gesagt: alle die ihr benötigt. Instagram, TikTok, LinkedIn primär. YouTube für Evergreen-Formate. Facebook als Recycling-Kanal. Welche Plattformen für euch wirklich Sinn machen, klären wir im Workshop. Nicht jede Plattform passt zu jeder Marke.

**Answer EN:**
_(leer)_

##### FAQ 5
**Question DE:** Was ist der Unterschied zwischen einem Workshop und einer Social-Media-Strategie?
**Question EN:** _(leer)_
**Answer DE:**
Eine Social-Media-Strategie sagt euch, welche Plattformen und welche Frequenz. Unser Workshop sagt euch, welche Geschichten ihr dort erzählen sollt und wie. Die zwei ergänzen sich, sie ersetzen sich nicht.

**Answer EN:**
_(leer)_

##### FAQ 6
**Question DE:** Auch für ganz kleine Unternehmen?
**Question EN:** _(leer)_
**Answer DE:**
EPUs aufwärts. Wir haben das Format bewusst so gebaut, dass es für ein einzelnes Unternehmen mit klarer Persönlichkeit (siehe Säule 01) wirtschaftlich passt. Wenn ihr noch ganz am Anfang steht und unsicher seid, ob Social Media überhaupt der richtige Hebel ist, sagen wir das auch im Erstgespräch.

**Answer EN:**
_(leer)_

#### 12. `cta`
_(block-id: 69fb44abc5ee5d4dd4325ce2)_

**Headline DE:** Lass uns reden.
**Headline EN:** _(leer)_
**Subline DE:** Erzählt uns von eurer Marke. Wir hören zu.
**Subline EN:** _(leer)_
_Variant: form_

---

#### SEO

**Meta Title DE:** _(leer)_
**Meta Title EN:** _(leer)_

**Meta Description DE:** _(leer)_
**Meta Description EN:** _(leer)_

---

### 9. Brand Documentary

- **ID:** 12
- **URL-Path:** `/agency/brand-documentary`
- **Slug:** `brand-documentary`
- **Area:** agency
- **Visibility:** public

**Title DE:** Brand Documentary
**Title EN:** _(leer)_

#### Sections (1)

#### 1. `hero`
_(block-id: 69f222be47d4aa108a1f46ac)_

_Variant: reduced_

**Headline DE:** _(leer)_
**Headline EN:** _(leer)_
**Subline DE:** _(leer)_
**Subline EN:** _(leer)_

---

#### SEO

**Meta Title DE:** _(leer)_
**Meta Title EN:** _(leer)_

**Meta Description DE:** _(leer)_
**Meta Description EN:** _(leer)_

---

### 10. Branded Entertainment

- **ID:** 10
- **URL-Path:** `/agency/branded-entertainment`
- **Slug:** `branded-entertainment`
- **Area:** agency
- **Visibility:** public

**Title DE:** Branded Entertainment
**Title EN:** _(leer)_

#### Sections (7)

#### 1. `hero`
_(block-id: 69f222ec47d4aa108a1f46b0)_

_Variant: landing_

**Headline DE:** _(leer)_
**Headline EN:** _(leer)_
**Subline DE:** _(leer)_
**Subline EN:** _(leer)_

#### 2. `bold-statement`
_(block-id: 69fc5e13e5a6e3838c36f4ce)_

**Line 1 DE:** Werte,
**Line 1 EN:** _(leer)_
**Line 2 (Copper) DE:** ohne zu verkaufen
**Line 2 (Copper) EN:** _(leer)_
**Tagline DE:** Branded Entertainment für Marken, die als Publisher denken.
**Tagline EN:** _(leer)_

#### 3. `problem-statement`
_(block-id: 69fc60ace5a6e3838c36f4d0)_

**Eyebrow DE:** Was wirkt.
**Eyebrow EN:** _(leer)_
**Headline DE:** Marken werden zu Publishern.
**Headline EN:** _(leer)_
**Support Text DE:** Lego hat einen kompletten Entertainment-Zweig aufgebaut. Patagonia und Red Bull produzieren Filme und Serien wie Verlagshäuser. Family-zentrierte Marken erkennen: eigene Geschichten binden stärker als jede Kampagne. Reichweite entsteht hier nicht durch Werbedruck, sondern durch Erzählungen, die das Publikum freiwillig sucht.
**Support Text EN:** _(leer)_

#### 4. `magazine-manifest`
_(block-id: 69fc60e0e5a6e3838c36f4d2)_

**Eyebrow DE:** Position.
**Eyebrow EN:** _(leer)_
**Sub-Headline DE:** Marke als Verlagshaus.
**Sub-Headline EN:** _(leer)_
**Lead DE:** Branded Entertainment ist die Disziplin für Marken, die wissen: Reichweite entsteht durch Substanz und durch eigene Kanäle, nicht durch Werbedruck.
**Lead EN:** _(leer)_
**Body DE:**
Eine Marke, die ein Entertainment-Format ermöglicht, agiert wie ein Verlagshaus. Sie tritt als Absender und Botschafter auf, niemals als Verkäufer. Die Geschichte muss für sich tragen können. Werte werden über die Erzählung transportiert, nicht über Logo-Einblendungen oder Produktplatzierung.
Reichweite kommt aus zwei Quellen: aus den eigenen Kanälen der Marke und aus der Wucht der Geschichte, die das Publikum freiwillig weiterträgt. Besonders Family-zentrierte Marken finden hier ein Format, das hält. Kinder, Jugendliche, Familien akzeptieren keine Werbung in Geschichten. Aber sie binden sich an Marken, die ihnen Geschichten ermöglichen, die für sich stehen.

**Body EN:**
_(leer)_

##### Pull Quote
**Quote DE:** _(leer)_
**Quote EN:** _(leer)_

#### 5. `text-section`
_(block-id: 69fc6149e5a6e3838c36f4d4)_

**Eyebrow DE:** Handwerk.
**Eyebrow EN:** _(leer)_
**Headline DE:** Storytelling liegt in der DNA von Little Lights.
**Headline EN:** _(leer)_
**Content DE:**
Bevor Little Lights als Studio entstand, gab es vier Jahre Regie im Kinderfernsehen. Kein Format hat strengere Maßstäbe an Storytelling: junge Zuseher halten keine Geschichte aus, die nicht trägt. Aus dieser Schule kommt das Studio, mit der gleichen Disziplin, die heute Branded-Entertainment-Formate für Marken trägt.
Wir arbeiten gleichzeitig an Projekten für Marken und an eigenen Entertainment-Projekten. Im Studio entstehen Kurz-, Lang- und Dokumentarfilme. Wir veröffentlichten die Helena Flinn Trilogie, eine Buchreihe für Middle-Grade-Leser. Die gleichen Hände, die eine Buchszene überarbeiten oder die Plot-Struktur eines Kurzfilms entwerfen, schreiben auch das Treatment für die Animationsserie einer Marke. Die Disziplin ist eine.
Diese Erfahrung mit Geschichten für junge und gemischte Zielgruppen macht uns zum natürlichen Partner für Marken, deren Publikum Familien sind.

**Content EN:**
_(leer)_

#### 6. `projects-grid`
_(block-id: 69fc61c8e5a6e3838c36f4d6)_

**Eyebrow DE:** Ausgewählte Formate
**Eyebrow EN:** _(leer)_
**Big Headline DE:** Marken, die
Geschichten ermöglichen.
**Big Headline EN:** _(leer)_
_Layout: grid · Aspect: landscape · Cols: 3_

#### 7. `cta`
_(block-id: 69fc620be5a6e3838c36f4d8)_

**Headline DE:** Plant ihr ein Format, das nichts verkauft?
**Headline EN:** _(leer)_
**Subline DE:** Wir helfen euch, es zu finden und zu erzählen.
**Subline EN:** _(leer)_
_Variant: form_

---

#### SEO

**Meta Title DE:** _(leer)_
**Meta Title EN:** _(leer)_

**Meta Description DE:** _(leer)_
**Meta Description EN:** _(leer)_

---

### 11. Werbespot

- **ID:** 9
- **URL-Path:** `/agency/commercial`
- **Slug:** `commercial`
- **Area:** agency
- **Visibility:** public

**Title DE:** Werbespot
**Title EN:** _(leer)_

#### Sections (8)

#### 1. `hero`
_(block-id: 69f21fcf47d4aa108a1f4692)_

_Variant: landing_

**Headline DE:** _(leer)_
**Headline EN:** _(leer)_
**Subline DE:** _(leer)_
**Subline EN:** _(leer)_

#### 2. `bold-statement`
_(block-id: 69fb11f49b538300f9b93e80)_

**Line 1 DE:** Werbung
**Line 1 EN:** _(leer)_
**Line 2 (Copper) DE:** mit Haltung.
**Line 2 (Copper) EN:** _(leer)_
**Tagline DE:** Werbespots & Kampagnen Wien.
**Tagline EN:** _(leer)_

#### 3. `problem-statement`
_(block-id: 69fb121f9b538300f9b93e82)_

**Eyebrow DE:** Was wirkt.
**Eyebrow EN:** _(leer)_
**Headline DE:** Visuelles Spektakel hält die Aufmerksamkeit. Haltung hält den Gedanken danach.
**Headline EN:** _(leer)_
**Support Text DE:** Neunzig Prozent der Werbung pendelt zwischen lautem Spektakel und billiger Reklame. Beides funktioniert kurz, beides verschwindet schnell. Was bleibt, ist nicht die Lautstärke, sondern was eine Marke wirklich meint.
**Support Text EN:** _(leer)_

#### 4. `magazine-manifest`
_(block-id: 69fb12639b538300f9b93e84)_

**Eyebrow DE:** Unsere Antwort.
**Eyebrow EN:** _(leer)_
**Sub-Headline DE:** Auch in kurzer Zeit lässt sich der Markenkern zeigen.
**Sub-Headline EN:** _(leer)_
**Lead DE:** Werbung wird oft als groß, teuer und distanziert wahrgenommen. Wir sehen das anders.
**Lead EN:** _(leer)_
**Body DE:**
Die meisten Werbespots bewegen sich in zwei Lagern: visuelles Spektakel ohne Tiefgang, oder billige Reklame. Das eine kostet viel und bleibt hohl, das andere kostet wenig und ärgert. Wir gehen einen anderen Weg. In dreißig Sekunden, in zwei Minuten, in jedem Format konzentrieren wir uns auf den Kern der Marke und erzählen eine authentische Geschichte mit Haltung und Werten.
Unser Anspruch ist menschlich, emotional, nahbar. Technik und Bildqualität sind wichtig, aber eine Story-driven Idee ist wichtiger. Auch ein Spot von dreißig Sekunden kann eine Marke verständlich machen, wenn man die richtige Geschichte findet - eine, die der Zuseher in einem Moment ernst nehmen kann.

**Body EN:**
_(leer)_

##### Pull Quote
**Quote DE:** _(leer)_
**Quote EN:** _(leer)_

#### 5. `magazine-manifest`
_(block-id: 69fb12bc9b538300f9b93e86)_

**Eyebrow DE:** Für Agenturen.
**Eyebrow EN:** _(leer)_
**Sub-Headline DE:** Eure Idee, unsere Produktion.
**Sub-Headline EN:** _(leer)_
**Lead DE:** Manche Unternehmen kommen direkt zu uns, andere mit ihrer Werbeagentur an der Seite. Beide Wege funktionieren.
**Lead EN:** _(leer)_
**Body DE:**
Wenn die Idee bei der Agentur entsteht, sind wir kreativer Produktionspartner: erfahrenes Team, klare Kommunikation, mitdenkende Umsetzung. In der Regie-Auswahl achten wir auf Stärken, die zum Werk passen, und bringen unsere kreative Sicht dort ein, wo sie das Konzept besser macht. Ohne unnötiges Ego, ohne Konzept-Wettstreit.
Was uns dabei auszeichnet: was wir vor der Kamera erzählen, leben wir auch dahinter. Authentizität, Ehrlichkeit und wertebasiertes Handeln gelten nicht nur für die fertigen Bilder, sondern für jeden Schritt davor: Set-Atmosphäre, Kommunikation, Umgang mit Crew. Das macht in der finalen Arbeit einen Unterschied, ob man ihn direkt sieht oder nur spürt.
Wir arbeiten gerne mit bestehenden Werbeagenturen an Kampagnen und Projekten zusammen. Das steht sich nicht im Weg.

**Body EN:**
_(leer)_

##### Pull Quote
**Quote DE:** _(leer)_
**Quote EN:** _(leer)_

#### 6. `projects-grid`
_(block-id: 69fb15999b538300f9b93e92)_

**Eyebrow DE:** Ausgewählte Projekte.
**Eyebrow EN:** _(leer)_
**Big Headline DE:** Werbung,
die nicht laut sein muss.
**Big Headline EN:** _(leer)_
_Layout: grid · Aspect: landscape · Cols: 3_

#### 7. `faq`
_(block-id: 69fb14619b538300f9b93e88)_

**Eyebrow DE:** Klartext.
**Eyebrow EN:** _(leer)_
**Headline DE:** Was am häufigsten gefragt wird.
**Headline EN:** _(leer)_

##### FAQ 1
**Question DE:** Was kostet ein Werbespot?
**Question EN:** _(leer)_
**Answer DE:**
Die Spanne ist groß. Ein einzelner Online-Spot mit fokussiertem Setup ist eine andere Größenordnung als eine TV-Kampagne mit mehreren Cut-Downs und größerem Stab. Was den Preis konkret bestimmt: Konzepttiefe, Drehumfang, Locations, Anzahl der Cut-Downs, Postproduktion und ob die Idee bei euch, bei einer Agentur oder bei uns entsteht. Wir kalkulieren transparent nach einem ersten Konzeptgespräch.

**Answer EN:**
_(leer)_

##### FAQ 2
**Question DE:** Können wir mit unserer Werbeagentur kommen?
**Question EN:** _(leer)_
**Answer DE:**
Ja, regelmäßig. Wir arbeiten oft als Filmproduktion für Werbeagenturen und setzen deren Konzepte um - eingebunden in deren Prozess, mit klarer Rollenverteilung. Kein Konzept-Wettstreit, keine kreative Konkurrenz. Wir machen euch die Produktion einfacher.

**Answer EN:**
_(leer)_

##### FAQ 3
**Question DE:** Wie unterscheidet sich euer Werbespot-Ansatz?
**Question EN:** _(leer)_
**Answer DE:**
Wir glauben, dass auch in kurzer Zeit Substanz möglich ist. Statt visuellem Spektakel oder lauter Reklame fokussieren wir auf den Markenkern und erzählen eine Geschichte mit Haltung. Das ist menschlicher, emotionaler und langfristig wirksamer. Technik ist Voraussetzung, Story ist Differenz.

**Answer EN:**
_(leer)_

##### FAQ 4
**Question DE:** Wie lange dauert eine Spot-Produktion?
**Question EN:** _(leer)_
**Answer DE:**
Typischerweise vier bis acht Wochen von Konzeptfreigabe bis Master, je nach Drehumfang und Anzahl der Cut-Downs. Pre-Production drei bis vier Wochen, Drehtage ein bis drei, Postproduktion zwei bis drei Wochen. Bei kürzeren Online-Spots oder Pre-Rolls schneller, bei aufwändigen TV-Kampagnen länger.

**Answer EN:**
_(leer)_

#### 8. `cta`
_(block-id: 69fb16559b538300f9b93e94)_

**Headline DE:** Sprechen wir über euren Spot.
**Headline EN:** _(leer)_
**Subline DE:** Direkt oder mit Agentur - beide Wege gehen wir gerne. Ein Gespräch, kein Pitch.
**Subline EN:** _(leer)_
_Variant: form_

---

#### SEO

**Meta Title DE:** _(leer)_
**Meta Title EN:** _(leer)_

**Meta Description DE:** _(leer)_
**Meta Description EN:** _(leer)_

---

### 12. Employer Branding

- **ID:** 7
- **URL-Path:** `/agency/employer-branding`
- **Slug:** `employer-branding`
- **Area:** agency
- **Visibility:** public

**Title DE:** Employer Branding
**Title EN:** _(leer)_

#### Sections (9)

#### 1. `hero`
_(block-id: 69f21e7647d4aa108a1f4688)_

_Variant: landing_

**Headline DE:** _(leer)_
**Headline EN:** _(leer)_
**Subline DE:** _(leer)_
**Subline EN:** _(leer)_

#### 2. `bold-statement`
_(block-id: 69f8f0c1161c9929d14fc28a)_

**Line 1 DE:** Echte Menschen.
**Line 1 EN:** _(leer)_
**Line 2 (Copper) DE:** Echte Stories.
**Line 2 (Copper) EN:** _(leer)_
**Tagline DE:** Employer Branding Film aus Wien.
**Tagline EN:** _(leer)_

#### 3. `magazine-manifest`
_(block-id: 69f8f0db161c9929d14fc28c)_

**Eyebrow DE:** Unsere Antwort.
**Eyebrow EN:** _(leer)_
**Sub-Headline DE:** Wir bauen Employer Branding Formate, in denen echte Menschen echt wirken.
**Sub-Headline EN:** _(leer)_
**Lead DE:** Seit über zwölf Jahren spezialisieren wir uns auf Employer Branding Filme. Vom einzelnen Recruiting-Video bis zur fortlaufenden Karriere-Serie.
**Lead EN:** _(leer)_
**Body DE:**
_(leer)_

**Body EN:**
_(leer)_

##### Pull Quote
**Quote DE:** _(leer)_
**Quote EN:** _(leer)_
_Attribution: Michael Sagmeister, People & Culture Development · Strabag_

#### 4. `stats`
_(block-id: 69f8f259161c9929d14fc28e)_

**Headline DE:** Employer Branding
**Headline EN:** _(leer)_
**Headline Accent DE:** in Zahlen
**Headline Accent EN:** _(leer)_

##### Stat 1
_Number: 150+_
**Label DE:** Strabag Karrierestories
**Label EN:** _(leer)_

##### Stat 2
_Number: 24_
**Label DE:** Greiner Walks Episoden
**Label EN:** _(leer)_

##### Stat 3
_Number: 900+_
**Label DE:** Interviews International
**Label EN:** _(leer)_

##### Stat 4
_Number: 12+_
**Label DE:** Jahre Spezialisierung
**Label EN:** _(leer)_

#### 5. `text-section`
_(block-id: 69f8f2ea161c9929d14fc292)_

**Eyebrow DE:** _(leer)_
**Eyebrow EN:** _(leer)_
**Headline DE:** Wie eine Employer Branding Serie entsteht.
**Headline EN:** _(leer)_
**Content DE:**
1. Konzept - Wir starten mit einer Workshop-Phase: Wer sind eure Menschen, was ist die Wahrheit eurer Kultur, welcher Format-Bogen trägt? Output ist kein Drehbuch, sondern ein Format-Konzept das skaliert.
2. Pilotepisode - Eine erste Episode ist zugleich Beweis und Lerngrundlage. Was funktioniert vor der Kamera? Welche Tonalität trifft? Wo halten Mitarbeiter:innen sich zurück? Die Pilotepisode entscheidet, ob aus dem Auftrag eine Reihe wird.
3. Serie - Mit dem validierten Format gehen wir in die Produktion mehrerer Episoden. Effizient, weil das Konzept steht. Authentisch, weil das Setup eingespielt ist.
4. Archiv - Aus den Episoden entsteht über Zeit ein Bewerber:innen-Archiv. Es altert nicht, weil dokumentarische Geschichten nicht verfallen. Es wird zur stärksten Recruiting-Ressource, die ihr besitzt.

**Content EN:**
_(leer)_

#### 6. `magazine-manifest`
_(block-id: 69f8f33e161c9929d14fc294)_

**Eyebrow DE:** Wo wir drehen.
**Eyebrow EN:** _(leer)_
**Sub-Headline DE:** Wien für Konzept und Schnitt. Eure Standorte für den Dreh.
**Sub-Headline EN:** _(leer)_
**Lead DE:** Konzept, Kundenkontakt und Post-Produktion bleiben bei uns. Den Dreh übernehmen regionale Crews, mit denen wir über Jahre Vertrauen aufgebaut haben.
**Lead EN:** _(leer)_
**Body DE:**
Wir arbeiten mit Teams in Österreich und mit Produktionspartnern in Deutschland, Europa und darüber hinaus. Dahinter stehen drei Gründe: Nachhaltigkeit, weil weniger Reisen weniger CO₂ bedeuten. Regionale Expertise, weil lokale Crews Sprache, Kultur und Genehmigungen kennen. Und schlichtweg Effizienz, weil ein eingespieltes Team vor Ort oft schneller produziert.
Über die Jahre haben wir ein Netz spezialisierter Teams aufgebaut. Vom zwei-köpfigen Regie- und Kamera-Setup für intime Mitarbeiter-Interviews bis zur Service-Produktion mit lokalen Genehmigungen, Fixern und Equipment. Für ein internationales Roll-out haben wir über 100 Interviews realisiert, gedreht von Crews in Europa, den USA und China. Koordiniert aus Wien, mit einheitlicher Bildsprache, einheitlicher Tonalität, einheitlicher Schnittmethodik.
Für euch heißt das: ein Studio kümmert sich um Konzept und Endprodukt. Mehrere Crews drehen dort, wo eure Mitarbeiter:innen tatsächlich arbeiten.

**Body EN:**
_(leer)_

##### Pull Quote
**Quote DE:** _(leer)_
**Quote EN:** _(leer)_

#### 7. `projects-grid`
_(block-id: 69f8f3b2161c9929d14fc296)_

**Eyebrow DE:** Ausgewählte EB-Arbeiten
**Eyebrow EN:** _(leer)_
**Big Headline DE:** Was wir mit unseren Kunden 
gebaut haben.
**Big Headline EN:** _(leer)_
_Layout: grid · Aspect: landscape · Cols: 3_

#### 8. `faq`
_(block-id: 69f9e9fb9b538300f9b93e56)_

**Eyebrow DE:** Häufig gefragt
**Eyebrow EN:** _(leer)_
**Headline DE:** Häufige Fragen zu Emploayer Branding Filmen.
**Headline EN:** _(leer)_

##### FAQ 1
**Question DE:** Was kostet ein Employer Branding Film?
**Question EN:** _(leer)_
**Answer DE:**
Die Spanne ist groß, und eine pauschale Zahl wäre eine Schätzung ohne Grundlage. Was den Preis konkret bestimmt: das Format (einmaliger Film oder wachsende Reihe), Drehumfang und Locations, Tiefe der Postproduktion und ob ihr Konzeptarbeit mitbestellt. Ein einzelner Recruiting-Clip mit kleinem Setup ist eine andere Größenordnung als eine internationale Format-Serie mit mehreren Episoden. Wir kalkulieren transparent nach einem ersten Konzeptgespräch. Dort hören wir zuerst zu, bevor wir Zahlen nennen.

**Answer EN:**
_(leer)_

##### FAQ 2
**Question DE:** Wie lange dauert die Produktion?
**Question EN:** _(leer)_
**Answer DE:**
Von Briefing bis erstem Schnitt: vier bis acht Wochen für eine einzelne Episode. Format-Workshops vor dem ersten Dreh: ein bis zwei Tage. Reine Produktion einer Serie nach validiertem Konzept: ein bis drei Drehtage pro Episode-Block.

**Answer EN:**
_(leer)_

##### FAQ 3
**Question DE:** Produziert ihr auch außerhalb von Wien und Österreich?
**Question EN:** _(leer)_
**Answer DE:**
Ja. Konzept, Kundenkontakt und Post-Produktion liegen immer bei uns in Wien. Den Dreh selbst übernehmen regionale Teams, mit denen wir über Jahre zusammenarbeiten. Wir haben EB-Projekte in Österreich, Deutschland, weiteren europäischen Ländern, in den USA und in China realisiert, mit über 100 Interviews allein in einem internationalen Roll-out. Das spart Reisekosten, reduziert CO₂ und macht Roll-outs an mehreren Standorten parallel möglich, ohne dass die Bildsprache uneinheitlich wird.

**Answer EN:**
_(leer)_

##### FAQ 4
**Question DE:** Wie findet man eine gute Employer-Branding-Filmproduktion?
**Question EN:** _(leer)_
**Answer DE:**
Schaut euch in den Referenzen die Menschen an, nicht die Bildkomposition. Bewerber:innen merken denselben Unterschied. Und vertraut dem ersten Gespräch: ein Studio, das zuhört bevor es pitcht, wird euch auch im Projekt verstehen.

**Answer EN:**
_(leer)_

##### FAQ 5
**Question DE:** Was ist der Unterschied zwischen einem EB-Film und einem Imagefilm?
**Question EN:** _(leer)_
**Answer DE:**
Ein Imagefilm zeigt das Unternehmen nach außen - wofür es steht, was es kann. Ein EB-Film zeigt das Unternehmen von innen - wer dort arbeitet, wie der Alltag aussieht, was die Menschen verbindet. EB-Filme richten sich in den meisten Fällen an Bewerber:innen, Imagefilme an alle.

**Answer EN:**
_(leer)_

##### FAQ 6
**Question DE:** Können wir mit einem einzelnen Film starten?
**Question EN:** _(leer)_
**Answer DE:**
Ja. Jede unserer langfristigen Partnerschaften hat mit genau einem Projekt begonnen. Wenn der erste Film trägt, wächst daraus oft eine Reihe. Wenn nicht, bleibt es ein gutes einzelnes Werk.

**Answer EN:**
_(leer)_

#### 9. `cta`
_(block-id: 69f8f51c161c9929d14fc29a)_

**Headline DE:** Sprechen wir über euer EB.
**Headline EN:** _(leer)_
**Subline DE:** Ein 30-Minuten-Gespräch, kein Pitch. Wir hören zu, fragen viel, und sagen ehrlich was wir machen würden.
**Subline EN:** _(leer)_
_Variant: form_

---

#### SEO

**Meta Title DE:** Employer Branding Film Wien | 150+ Karrierestories | Little Lights
**Meta Title EN:** _(leer)_

**Meta Description DE:** 150+ Karrierestories, eigene Formatentwicklung, regionale Crews weltweit. Die erfahrenste EB-Filmproduktion in Wien.
**Meta Description EN:** _(leer)_

---

### 13. Imagefilm

- **ID:** 8
- **URL-Path:** `/agency/imagefilm`
- **Slug:** `imagefilm`
- **Area:** agency
- **Visibility:** public

**Title DE:** Imagefilm
**Title EN:** _(leer)_

#### Sections (10)

#### 1. `hero`
_(block-id: 69f21f8747d4aa108a1f4690)_

_Variant: landing_

**Headline DE:** _(leer)_
**Headline EN:** _(leer)_
**Subline DE:** _(leer)_
**Subline EN:** _(leer)_

#### 2. `bold-statement`
_(block-id: 69f9f1e99b538300f9b93e64)_

**Line 1 DE:** Imagefilm.
**Line 1 EN:** _(leer)_
**Line 2 (Copper) DE:** Werte zuerst.
**Line 2 (Copper) EN:** _(leer)_
**Tagline DE:** Imagefilm Wien.
**Tagline EN:** _(leer)_

#### 3. `problem-statement`
_(block-id: 69f9f2239b538300f9b93e66)_

**Eyebrow DE:** Was zählt.
**Eyebrow EN:** _(leer)_
**Headline DE:** Wer eine Marke spüren will, will keine Folien sehen.
**Headline EN:** _(leer)_
**Support Text DE:** Zuseher:innen merken, wenn ein Imagefilm aus zufälligen Drohnen-Aufnahmen, Inserts und Besprechungsraum-Bildern zusammengesetzt ist. Sie merken auch sofort, wenn eine Geschichte trägt. Schöne Bilder kann heute jedes Smartphone. Eine Geschichte, die im Kopf bleibt - das ist der Unterschied.
**Support Text EN:** _(leer)_

#### 4. `magazine-manifest`
_(block-id: 69f9f2559b538300f9b93e68)_

**Eyebrow DE:** Unsere Antwort.
**Eyebrow EN:** _(leer)_
**Sub-Headline DE:** Wir bauen Imagefilme von der Wurzel. Werte zuerst, Story zuerst, Bilder danach.
**Sub-Headline EN:** _(leer)_
**Lead DE:** Imagefilm ist nicht Maschinen, nicht Produkte, nicht Kennzahlen. Imagefilm ist die Antwort auf eine Frage: warum sollte sich jemand mit dieser Marke verbinden?
**Lead EN:** _(leer)_
**Body DE:**
Wir starten nie mit der Produktbroschüre. Wir starten mit den Fragen, die Bewerber:innen, Kund:innen und Partner:innen wirklich stellen: Welches Problem löst dieses Unternehmen für mich? Kann ich mich mit den Werten identifizieren? Warum sollte ich diese Firma toll finden? Wenn diese Basis steht, können Dienstleistungen und Produkte folgen, dann tragen sie eine Bedeutung statt einfach gezeigt zu werden.
Unsere wichtigste Zutat ist nicht die Kamera, sondern die Story. Mit Emotion verknüpfte Information bleibt im Kopf. Eine PowerPoint mit hundert Zahlen nicht. Deshalb ist die Story für uns auch der Sortier-Filter: auf welche zwei oder drei Kernbotschaften fokussieren wir uns? Zu viel Inhalt heißt zu wenig Erinnerung.
Schöne Filme kann jeder mit Smartphone. Eine Geschichte, die im Kopf bleibt und die Ziele erreicht, das machen wir seit über zwölf Jahren.

**Body EN:**
_(leer)_

##### Pull Quote
**Quote DE:** _(leer)_
**Quote EN:** _(leer)_

#### 5. `dual-path`
_(block-id: 69fc53e6e5a6e3838c36f4c8)_

**Section Eyebrow DE:** Zwei Pfade.
**Section Eyebrow EN:** _(leer)_
**Section Headline DE:** Eine Frage, die vor dem Konzept steht.
**Section Headline EN:** _(leer)_
**Section Intro DE:** Inszeniert oder dokumentarisch. Beide Wege sind legitim, beide brauchen anderes Handwerk. Die Wahl entscheidet über Tonalität, Dauer und wie der Film später weiterlebt.
**Section Intro EN:** _(leer)_

##### Path 1
**Eyebrow DE:** _(leer)_
**Eyebrow EN:** _(leer)_
**Headline DE:** Inszeniert.
**Headline EN:** _(leer)_
**Body DE:**
Der klassische Imagefilm. Treatment, Casting, Drehbuch, Sprecher. Werte zuerst, Story zuerst, Bilder danach. 60 bis 180 Sekunden, präzise inszeniert, mit einem klaren dramaturgischen Bogen. Das Format trägt, wenn eine Marke ihre Haltung verdichten und einen konkreten emotionalen Anker setzen will. Wie zum Beispiel die I am Progress Kampagne oder der Strabag Imagefilm.

**Body EN:**
_(leer)_

##### Path 2
**Eyebrow DE:** _(leer)_
**Eyebrow EN:** _(leer)_
**Headline DE:** Dokumentarisch.
**Headline EN:** _(leer)_
**Body DE:**
Recherche, Beobachtung, Treatments. 7 bis 15 Minuten oder in Serien-Episoden, plus Director's Cut, Brand Version, themenspezifische Cutdowns und Trailer. Die Marke ist nicht im Vordergrund, sie ermöglicht. Das Format trägt, wenn ein Thema Tiefe braucht und eine Marke sich selbst als Botschafter versteht. Zum Beispiel die dokumentarische Allianz Paralympics-Serie oder unsere Plastic Bank Manila Doku.

**Body EN:**
_(leer)_

##### Pull Quote
**Quote DE:** _(leer)_
**Quote EN:** _(leer)_

#### 6. `text-section`
_(block-id: 69f9f2d89b538300f9b93e6a)_

**Eyebrow DE:** _(leer)_
**Eyebrow EN:** _(leer)_
**Headline DE:** Wie ein Imagefilm bei uns entsteht.
**Headline EN:** _(leer)_
**Content DE:**
1. Briefing & Gespräch. Ein Briefing ist der Anfang, nicht das fertige Drehbuch. In einem ersten Gespräch klären wir die offenen Rahmenbedingungen - Ziel, Zielgruppe, Tonalität, Budget - und stellen die inhaltlichen Fragen, die das Konzept später tragen.
2. Konzept (2-3 Richtungen). Bei größeren Produktionen entwickeln wir zwei oder drei Konzept-Richtungen, mit dem Budgetrahmen im Hinterkopf. Ihr bekommt nicht eine Variante zum Abnicken, sondern echte Optionen, die unterschiedliche Geschichten erzählen. Die Wahl wird so eine bewusste Entscheidung statt ein Daumen-hoch.
3. Wahl & Produktion. Mit der gewählten Richtung gehen wir in die Detail-Konzeption, das Drehbuch und die Produktion. Konzept und Regie liegen in einer Hand, damit der Film die Handschrift bekommt, für die ihr uns beauftragt habt.

**Content EN:**
_(leer)_

#### 7. `magazine-manifest`
_(block-id: 69f9f3579b538300f9b93e6c)_

**Eyebrow DE:** Wo wir drehen.
**Eyebrow EN:** _(leer)_
**Sub-Headline DE:** Konzept und Regie aus einer Hand. Crew dort, wo der Film stattfindet.
**Sub-Headline EN:** _(leer)_
**Lead DE:** Bei größeren Imagefilm-Produktionen reist nur das Kernteam - Regie, Kamera, Producer. Die erweiterte Crew buchen wir lokal.
**Lead EN:** _(leer)_
**Body DE:**
Der Grund: ein starkes Konzept braucht eine konsistente Handschrift. Wenn ein zwanzig-köpfiges Team bei jedem Dreh anreist, geht die Handschrift im Logistik-Aufwand unter. Wenn ein kleines Kernteam reist und vor Ort eine erprobte Crew ergänzt, bleibt die Handschrift erhalten und der Aufwand im Rahmen.
Wir arbeiten mit Teams in Österreich und mit Produktionspartnern in Deutschland, Europa und darüber hinaus. Dahinter stehen drei Gründe: Nachhaltigkeit, weil weniger Reisen weniger CO₂ bedeuten. Regionale Expertise, weil lokale Crews Sprache, Kultur und Genehmigungen kennen. Und schlichtweg Effizienz, weil ein eingespieltes Team vor Ort schneller produziert als eines das anreist.

**Body EN:**
_(leer)_

##### Pull Quote
**Quote DE:** _(leer)_
**Quote EN:** _(leer)_

#### 8. `projects-grid`
_(block-id: 69f9f5eb9b538300f9b93e7e)_

**Eyebrow DE:** Ausgewählte Arbeiten
**Eyebrow EN:** _(leer)_
**Big Headline DE:** Imagefilme,
die im Kopf bleiben.
**Big Headline EN:** _(leer)_
_Layout: grid · Aspect: landscape · Cols: 3_

#### 9. `faq`
_(block-id: 69f9f3a99b538300f9b93e6e)_

**Eyebrow DE:** Häufige Gefragt.
**Eyebrow EN:** _(leer)_
**Headline DE:** Die häufigsten Fragen zum Imagefilm.
**Headline EN:** _(leer)_

##### FAQ 1
**Question DE:** Was kostet ein Imagefilm?
**Question EN:** _(leer)_
**Answer DE:**
Die Spanne ist groß, und eine pauschale Zahl wäre eine Schätzung ohne Grundlage. Wir haben Imagefilme im fünfstelligen Bereich produziert und im sechsstelligen. Was den Preis konkret bestimmt: Konzepttiefe, Drehumfang und Locations, Anzahl der Drehtage, Postproduktion und ob ihr animierte oder dokumentarische Elemente wollt. Wir kalkulieren transparent nach einem ersten Konzeptgespräch.

**Answer EN:**
_(leer)_

##### FAQ 2
**Question DE:** Warum solltet ihr einen groben Budgetrahmen nennen?
**Question EN:** _(leer)_
**Answer DE:**
Weil ehrliche Konzepte ohne Rahmen nicht möglich sind. Ein Konzept für 8.000 Euro sieht anders aus als eines für 80.000 - nicht weil die Story unterschiedlich gut ist, sondern weil die Mittel unterschiedlich sind. Ein grober Rahmen erlaubt uns, von Anfang an in die richtige Richtung zu denken: in Tonalität, Aufwand und Format. Ohne ihn raten wir, mit ihm können wir konkret werden.

**Answer EN:**
_(leer)_

##### FAQ 3
**Question DE:** Müssen alle Stakeholder im Imagefilm vorkommen?
**Question EN:** _(leer)_
**Answer DE:**
Nein. Ein Imagefilm der die Wünsche von fünfzehn Personen aus sieben Abteilungen vereinen will, hat am Ende keinen Fokus mehr. Eine starke Story braucht zwei oder drei Kernbotschaften, nicht zwanzig. Welche das sind, ist eine strategische Entscheidung am Anfang des Konzepts, keine demokratische Abstimmung am Schluss.

**Answer EN:**
_(leer)_

##### FAQ 4
**Question DE:** Was muss alles im Imagefilm zu sehen sein?
**Question EN:** _(leer)_
**Answer DE:**
Genau das, was die Story trägt - und sonst nichts. Der schöne Besprechungsraum, das neue Bürogebäude, die Auszeichnung an der Wand: alles legitim, aber nur wenn es Teil der Geschichte ist. Wenn nicht, gehört es eher auf die Webseite oder in die Imagebroschüre.

**Answer EN:**
_(leer)_

##### FAQ 5
**Question DE:** Wie lange dauert die Produktion?
**Question EN:** _(leer)_
**Answer DE:**
Von Briefing bis Schnittfreigabe: typischerweise sechs bis zwölf Wochen für einen einzelnen Imagefilm. Konzept-Phase: ein bis drei Wochen. Drehtage: ein bis fünf, je nach Umfang. Postproduktion: zwei bis vier Wochen.

**Answer EN:**
_(leer)_

##### FAQ 6
**Question DE:** Was ist der Unterschied zwischen einem Imagefilm und einem Werbespot?
**Question EN:** _(leer)_
**Answer DE:**
Beide haben Story im Zentrum, sie unterscheiden sich in Reichweite und Tiefe. Ein Werbespot will in dreißig Sekunden breite Aufmerksamkeit gewinnen - ein Hook, ein Bild, eine Botschaft, die hängenbleibt. Ein Imagefilm bittet um zwei bis vier Minuten Zeit, um eine Marke wirklich kennenzulernen. Werbespot ist die Einladung, Imagefilm das Kennenlernen. Beide brauchen die gleiche Sorgfalt im Konzept, beide arbeiten mit Emotion.

**Answer EN:**
_(leer)_

#### 10. `cta`
_(block-id: 69f9f5549b538300f9b93e7c)_

**Headline DE:** Sprechen wir über euren Imagefilm.
**Headline EN:** _(leer)_
**Subline DE:** Ein 30-Minuten-Gespräch, kein Pitch. Ihr erzählt, wir hören zu, und sagen ehrlich was wir machen würden.
**Subline EN:** _(leer)_
_Variant: form_

---

#### SEO

**Meta Title DE:** _(leer)_
**Meta Title EN:** _(leer)_

**Meta Description DE:** _(leer)_
**Meta Description EN:** _(leer)_

---

### 14. Sustainability

- **ID:** 11
- **URL-Path:** `/agency/sustainability`
- **Slug:** `sustainability`
- **Area:** agency
- **Visibility:** public

**Title DE:** Sustainability
**Title EN:** _(leer)_

#### Sections (8)

#### 1. `hero`
_(block-id: 69f222de47d4aa108a1f46ae)_

_Variant: landing_

**Headline DE:** _(leer)_
**Headline EN:** _(leer)_
**Subline DE:** _(leer)_
**Subline EN:** _(leer)_

#### 2. `bold-statement`
_(block-id: 69fb2cf59b538300f9b93e96)_

**Line 1 DE:** Nachhaltigkeit,
**Line 1 EN:** _(leer)_
**Line 2 (Copper) DE:** ehrlich erzählt.
**Line 2 (Copper) EN:** _(leer)_
**Tagline DE:** Sustainability Communication
**Tagline EN:** _(leer)_

#### 3. `problem-statement`
_(block-id: 69fb2d199b538300f9b93e98)_

**Eyebrow DE:** Die Hürde.
**Eyebrow EN:** _(leer)_
**Headline DE:** Nachhaltigkeitskommunikation steht und fällt mit Glaubwürdigkeit.
**Headline EN:** _(leer)_
**Support Text DE:** Marketing-Sprech wirkt hier sofort gegen die Marke. Was zählt, sind ehrliche Worte und Menschen, die hinter dem Versprechen stehen.
**Support Text EN:** _(leer)_

#### 4. `magazine-manifest`
_(block-id: 69fb2d489b538300f9b93e9a)_

**Eyebrow DE:** Unsere Antwort.
**Eyebrow EN:** _(leer)_
**Sub-Headline DE:** _(leer)_
**Sub-Headline EN:** _(leer)_
**Lead DE:** Geschichten, die mit Menschen anfangen.
**Lead EN:** _(leer)_
**Body DE:**
Wir nehmen den Marketing-Sprech zurück. Wir hören zu, bevor wir formulieren. Wir lassen Menschen reden, die wirklich etwas zu sagen haben. Das klingt selbstverständlich, ist in der Nachhaltigkeitskommunikation aber der wichtigste Move. Hier fällt jede schief gewählte Vokabel sofort als Pose auf.
Auf den Philippinen haben wir eine Woche lang die Sammlerinnen von Plastic Bank in den Barangays von Manila begleitet. Geplant war ein Drehbuch, gedreht haben wir, was vor uns geschah. Daraus ist ein Dokumentarfilm geworden, der die Realität zeigt, ohne sie zu instrumentalisieren, und der die wirtschaftliche Logik einer Circular Economy genauso klar macht wie die menschlichen Geschichten dahinter.
Manchmal verlangt das Thema das unbequemste Format. Bei den Greiner Hard Talks hat ein Plastikverarbeiter seine eigene Führungsebene vor die Kamera gebeten, um die härtesten Fragen seiner Branche zu stellen. Wie reduziert man Emissionen, wenn das Kerngeschäft nicht inhärent grün ist? Sechs C-Levels, kein Ausweichen. Der Beweis, dass Glaubwürdigkeit auch dort möglich ist, wo es unbequem wird.
Bei anderen Kunden geht es weniger um die kontroverse Frage und mehr um Tiefe und Reichweite. Mitarbeitende, die in ihrem Arbeitsalltag konkret etwas bewegen, vor der Kamera. Über die Jahre sind so Hunderte Interviews quer über drei Kontinente entstanden, immer mit der gleichen Grundregel. Story und Werte zuerst. Bilder danach.
So entsteht Nachhaltigkeitskommunikation, die das Risiko von Greenwashing minimiert, ohne ihren Schwung zu verlieren. Glaubwürdig, weil sie aus dem Unternehmen selbst kommt. Sehenswert, weil eine gute Geschichte gut aussehen darf.

**Body EN:**
_(leer)_

##### Pull Quote
**Quote DE:** Wir haben die Menschen bei Greiner zu Wort kommen lassen. Mit Little Lights als Partner konnten wir Kommunikationsformate entwickeln, die stets authentisch und glaubwürdig bleiben.
**Quote EN:** _(leer)_
_Attribution: Alexander Berth - Diversity & Social Impact Manager, Greiner AG_

#### 5. `magazine-manifest`
_(block-id: 69fb2de49b538300f9b93e9c)_

**Eyebrow DE:** Warum dieses Thema.
**Eyebrow EN:** _(leer)_
**Sub-Headline DE:** _(leer)_
**Sub-Headline EN:** _(leer)_
**Lead DE:** Nachhaltigkeit ist für uns kein Auftragsthema.
**Lead EN:** _(leer)_
**Body DE:**
Wir arbeiten gerne an Nachhaltigkeitsfilmen, weil sich das Thema mit dem deckt, was wir als Studio selbst glauben. Ehrliche, menschliche Kommunikation, die gut aussehen darf, aber immer Story und Werte zuerst nimmt. Das ist für uns nicht Methode. Das ist Haltung.
Es geht nicht darum, ein Unternehmen über Nacht komplett umzudrehen. Es geht um bewusstes Handeln, um klare Ziele, um Schritte, die wirklich greifen. Lichtschalter abdrehen ist Symbolik. Eine intelligente Raumsteuerung, die large-scale dasselbe leistet, ist Wirkung. Beides hört sich gut an. Nur eines macht einen Unterschied.
Genau das interessiert uns auch in den Filmen, die wir zu dem Thema machen. Wir suchen die Maßnahme hinter der Botschaft. Den Menschen hinter der Position. Den Pfad, nicht den Sprung. So entstehen Formate, die nicht nur in der Kampagne stehen, sondern intern wie extern Bestand haben.
Wer ehrlich kommuniziert, muss nicht alles richtig machen. Aber das, was er zeigt, muss stimmen.

**Body EN:**
_(leer)_

##### Pull Quote
**Quote DE:** _(leer)_
**Quote EN:** _(leer)_

#### 6. `projects-grid`
_(block-id: 69fb2e3a9b538300f9b93e9e)_

**Eyebrow DE:** Ausgewählte Arbeiten
**Eyebrow EN:** _(leer)_
**Big Headline DE:** Geschichten,
die Haltung tragen.
**Big Headline EN:** _(leer)_
_Layout: grid · Aspect: landscape · Cols: 3_

#### 7. `faq`
_(block-id: 69fb2e7e9b538300f9b93ea0)_

**Eyebrow DE:** Klartext.
**Eyebrow EN:** _(leer)_
**Headline DE:** Was uns oft gefragt wird.
**Headline EN:** _(leer)_

##### FAQ 1
**Question DE:** Wie erzählt man Nachhaltigkeit, ohne in Greenwashing zu rutschen?
**Question EN:** _(leer)_
**Answer DE:**
Indem man die Maßnahmen erzählt, nicht die Pose. Indem man Menschen vor die Kamera bittet, die das Versprechen täglich tragen. Und indem man unbequemen Fragen nicht ausweicht. Ehrlichkeit hat einen sichtbaren Effekt auf die Glaubwürdigkeit eines Films, gerade weil sie selten ist.

**Answer EN:**
_(leer)_

##### FAQ 2
**Question DE:** Können wir das Thema angehen, obwohl unser Kerngeschäft nicht inhärent grün ist?
**Question EN:** _(leer)_
**Answer DE:**
Ja. Genau das war die Ausgangslage bei den Greiner Hard Talks: ein Plastikverarbeiter, der sich öffentlich der Frage nach seiner Rolle stellt. Das Format funktioniert, weil es nicht behauptet, nachhaltig zu sein, sondern transparent zeigt, wie das Unternehmen mit dieser Frage arbeitet. Haltung statt Hochglanz.

**Answer EN:**
_(leer)_

##### FAQ 3
**Question DE:** Welche Form passt zu welchem Anlass?
**Question EN:** _(leer)_
**Answer DE:**
Eine Doku gibt Raum für Tiefe (Plastic Bank Manila zeigt das). Ein Statement-Format bündelt Haltung in serieller Form. Eine Interview-Reihe quer durch die Belegschaft macht ein Thema breit erlebbar (Blue Plan, Sustainability Message). Welche Form passt, klären wir im ersten Gespräch, abhängig von Ziel, Zielgruppe und vorhandenen Stimmen.

**Answer EN:**
_(leer)_

##### FAQ 4
**Question DE:** Wie geht ihr mit sensiblen Drehsituationen um?
**Question EN:** _(leer)_
**Answer DE:**
Vorbereitung und Improvisation, beides muss stimmen. Bei Plastic Bank Manila sind wir mit Briefing und Plan in die Barangays gegangen und gleichzeitig bereit gewesen, alles loszulassen, wenn die Realität eine andere Geschichte erzählt. Begleiten statt inszenieren. Zuhören, bevor wir filmen. Ohne dieses Maß an Respekt entstehen die Geschichten gar nicht erst, die so eine Produktion eigentlich tragen soll.

**Answer EN:**
_(leer)_

##### FAQ 5
**Question DE:** Mit welcher Form starten?
**Question EN:** _(leer)_
**Answer DE:**
Oft mit dem Format, das den geringsten Aufwand und die höchste Authentizität verbindet: Mitarbeitende vor die Kamera, kurze Statements, einer nach dem anderen. Daraus entwickelt sich entweder eine Serie oder die nächste, größere Produktion. Wichtig ist nur, früh genug die Werte und das Ziel zu klären, damit der Film nicht im Schnittraum erfunden werden muss.

**Answer EN:**
_(leer)_

#### 8. `cta`
_(block-id: 69fb2f169b538300f9b93eac)_

**Headline DE:** Lasst uns sprechen.
**Headline EN:** _(leer)_
**Subline DE:** Erzählen wir eure Geschichte. Mit Substanz.
**Subline EN:** _(leer)_
_Variant: form_

---

#### SEO

**Meta Title DE:** _(leer)_
**Meta Title EN:** _(leer)_

**Meta Description DE:** _(leer)_
**Meta Description EN:** _(leer)_

---

### 15. Workshops & Keynotes

- **ID:** 21
- **URL-Path:** `/agency/workshops-keynotes`
- **Slug:** `workshops-keynotes`
- **Area:** agency
- **Visibility:** draft

**Title DE:** Workshops & Keynotes
**Title EN:** _(leer)_

#### Sections (0)

---

#### SEO

**Meta Title DE:** _(leer)_
**Meta Title EN:** _(leer)_

**Meta Description DE:** _(leer)_
**Meta Description EN:** _(leer)_

---

### 16. Film & Doku

- **ID:** 16
- **URL-Path:** `/creative-studio/film-doku`
- **Slug:** `film-doku`
- **Area:** creative
- **Visibility:** public

**Title DE:** Film & Doku
**Title EN:** _(leer)_

#### Sections (4)

#### 1. `hero`
_(block-id: 69f506ec4fde8d096c48250d)_

_Variant: landing_

**Headline DE:** _(leer)_
**Headline EN:** _(leer)_
**Subline DE:** _(leer)_
**Subline EN:** _(leer)_

#### 2. `bold-statement`
_(block-id: 69fd7cbe6b200d788a3fc264)_

**Line 1 DE:** Filme, die uns passen.
**Line 1 EN:** _(leer)_
**Line 2 (Copper) DE:** Und wir zu ihnen.
**Line 2 (Copper) EN:** _(leer)_
**Tagline DE:** _(leer)_
**Tagline EN:** _(leer)_

#### 3. `magazine-manifest`
_(block-id: 69fd7cea6b200d788a3fc266)_

**Eyebrow DE:** Unser Selbstverständnis.
**Eyebrow EN:** _(leer)_
**Sub-Headline DE:** _(leer)_
**Sub-Headline EN:** _(leer)_
**Lead DE:** Manche Filme machen wir für andere. Manche für uns.
**Lead EN:** _(leer)_
**Body DE:**
Im Studio arbeiten Regisseur:innen, Drehbuchautor:innen und Producer. Wir standen auf unzähligen Sets - im Auftrag und für eigene Stoffe, für Kurzfilme, Serien und lange Formate. Was wir hier machen, ist die Verlängerung dieser Arbeit unter unserem eigenen Namen.
Mit Little Lights entwickeln und produzieren wir Filme, die zu uns passen, und zu denen wir passen. Manche reichen wir in die Entwicklungsförderung ein. Manche tragen wir aus eigenem Engagement. Bei manchen reift der Stoff lange, bevor er auf einen Set geht.
Was hier entsteht, entsteht mit Zeit. Diese Seite wird mit unseren Filmen wachsen.

**Body EN:**
_(leer)_

##### Pull Quote
**Quote DE:** _(leer)_
**Quote EN:** _(leer)_

#### 4. `cta`
_(block-id: 69fd7d9a6b200d788a3fc268)_

**Headline DE:** Schreib uns.
**Headline EN:** _(leer)_
**Subline DE:** Wir lesen alles, was uns erreicht. Wer einen Stoff hat, der zu uns passen könnte, ist eingeladen.
**Subline EN:** _(leer)_
_Variant: form_

---

#### SEO

**Meta Title DE:** _(leer)_
**Meta Title EN:** _(leer)_

**Meta Description DE:** _(leer)_
**Meta Description EN:** _(leer)_

---

### 17. Publishing

- **ID:** 15
- **URL-Path:** `/creative-studio/publishing`
- **Slug:** `publishing`
- **Area:** creative
- **Visibility:** public

**Title DE:** Publishing
**Title EN:** _(leer)_

#### Sections (6)

#### 1. `hero`
_(block-id: 69f506624fde8d096c482509)_

_Variant: landing_

**Headline DE:** _(leer)_
**Headline EN:** _(leer)_
**Subline DE:** _(leer)_
**Subline EN:** _(leer)_

#### 2. `bold-statement`
_(block-id: 69fce3a92a51e9a7a597ef00)_

**Line 1 DE:** Ein kleiner Verlag aus Wien.
**Line 1 EN:** _(leer)_
**Line 2 (Copper) DE:** Mit Sorgfalt gebaut.
**Line 2 (Copper) EN:** _(leer)_
**Tagline DE:** Little Lights Studio Publishing
**Tagline EN:** _(leer)_

#### 3. `magazine-manifest`
_(block-id: 69fce3f92a51e9a7a597ef02)_

**Eyebrow DE:** Wie der Verlag entstand.
**Eyebrow EN:** _(leer)_
**Sub-Headline DE:** _(leer)_
**Sub-Headline EN:** _(leer)_
**Lead DE:** Wir machen seit über zwölf Jahren Filme. Verlegen tun wir, seit Helena Flinn 2024 erschien.
**Lead EN:** _(leer)_
**Body DE:**
2018 entstand im Studio eine Kurzgeschichte über Goblins, die unter Wien Träume bauen. Aus dieser Geschichte wurde fünf Jahre später ein Buch. Heute ist es eine Middle-Grade-Fantasy-Trilogie, von der zwei Bände erschienen sind und der dritte zum Jahresende folgt.
Verlegt haben wir die Bücher selbst. Little Lights Studio steht als offizieller Verlag in jedem Exemplar, distribuiert über Amazon KDP und IngramSpark, in Hardcover, Paperback und eBook. Was uns an dieser Arbeit interessiert, ist nicht das Volumen, sondern die Sorgfalt.
Aktuell verlegen wir genau ein Werk: die Helena Flinn Chronicles. Wenn der Verlag wächst, dann langsam und mit Bedacht. Bücher müssen zu uns passen, und wir zu den Büchern.

**Body EN:**
_(leer)_

##### Pull Quote
**Quote DE:** _(leer)_
**Quote EN:** _(leer)_

#### 4. `book-reviews`
_(block-id: 69fce7236b200d788a3fc24e)_

**Eyebrow DE:** Reviews.
**Eyebrow EN:** _(leer)_
**Headline DE:** Was Leser sagen.
**Headline EN:** _(leer)_

##### Featured Review
**Quote DE:** „A wholly original work of middle grade fantasy fiction. The metaphorical conflicts of sleep and the timeless search for connection weave neatly in Sokolar's liminal prose, blurring the edges of reality with evocative language, clever world-building, and a captivating plot that readers of all ages will find enchanting."
**Quote EN:** _(leer)_
**Source DE:** The Independent Review of Books
**Source EN:** _(leer)_

##### Review 1
**Quote DE:** „Middle grade fantasy unlike any other I have read. It examines the complexities of a very real set of health problems — sleep disorders — in a context of magical realism perfect for late elementary and early junior high readers, and even, in my case, adulthood."
**Quote EN:** _(leer)_
**Source DE:** Hannah Lindley
**Source EN:** _(leer)_

##### Review 2
**Quote DE:** „What better place to set a middle grade fantasy about a hidden dream world than Vienna, home of Sigmund Freud? Helena Flinn weaves the real-life science of dreams into a magical story of goblin engineers — exciting and easily accessible for middle grade readers."
**Quote EN:** _(leer)_
**Source DE:** Matthew Olson-Roy
**Source EN:** _(leer)_

##### Review 3
**Quote DE:** „A rare book that feels like a true adventure, yet still carries a deep sense of wonder and warmth. As a homeschooling mom, my children — ages 11, 8, 7, 5, and 4 — were all equally drawn in."
**Quote EN:** _(leer)_
**Source DE:** Jordie Slesarenko
**Source EN:** _(leer)_

##### Review 4
**Quote DE:** „An enchanting adventure about dreams, friendship, and belonging. The kind of book that makes you fall in love with reading all over again."
**Quote EN:** _(leer)_
**Source DE:** Mike Kren
**Source EN:** _(leer)_

##### Review 5
**Quote DE:** „The Helena Flinn Chronicles continue with magic, mystery, teamwork, and the power of dreams. The ending is jaw-dropping and will leave you with lots of questions and keen for the next in the Chronicles."
**Quote EN:** _(leer)_
**Source DE:** LoveReading4Kids
**Source EN:** _(leer)_

#### 5. `projects-grid`
_(block-id: 69fce8a06b200d788a3fc25c)_

**Eyebrow DE:** Was wir verlegen.
**Eyebrow EN:** _(leer)_
**Big Headline DE:** Helena Flinn Chronicles
**Big Headline EN:** _(leer)_
_Layout: pyramid · Aspect: landscape · Cols: 3_

#### 6. `cta`
_(block-id: 69fcea576b200d788a3fc262)_

**Headline DE:** Schreib uns gerne.
**Headline EN:** _(leer)_
**Subline DE:** Die Welt von Helena Flinn geht auf helenaflinn.com weiter. Wenn du dem Verlag etwas mitgeben willst, eine Nachricht hier reicht.
**Subline EN:** _(leer)_
_Variant: form_

---

#### SEO

**Meta Title DE:** _(leer)_
**Meta Title EN:** _(leer)_

**Meta Description DE:** _(leer)_
**Meta Description EN:** _(leer)_

---

### 18. Content Produktion

- **ID:** 14
- **URL-Path:** `/reels-stories/content-production`
- **Slug:** `content-production`
- **Area:** rs
- **Visibility:** public

**Title DE:** Content Produktion
**Title EN:** _(leer)_

#### Sections (9)

#### 1. `hero`
_(block-id: 69f5055f4fde8d096c482507)_

_Variant: landing_

**Headline DE:** _(leer)_
**Headline EN:** _(leer)_
**Subline DE:** _(leer)_
**Subline EN:** _(leer)_

#### 2. `bold-statement`
_(block-id: 69fca172a8642ed6214c6e1b)_

**Line 1 DE:** Strategie & Story zuerst.
**Line 1 EN:** _(leer)_
**Line 2 (Copper) DE:** Bilder folgen.
**Line 2 (Copper) EN:** _(leer)_
**Tagline DE:** Social Media Film-Produktion mit System.
**Tagline EN:** _(leer)_

#### 3. `problem-statement`
_(block-id: 69fca188a8642ed6214c6e1d)_

**Eyebrow DE:** Was nicht funktioniert.
**Eyebrow EN:** _(leer)_
**Headline DE:** Produktion ohne Strategie ist Aktion ohne Richtung.
**Headline EN:** _(leer)_
**Support Text DE:** Schöne Bilder allein bewegen heute niemanden mehr. Was wirkt, ist Content mit Plan: ein narrativer Kern, wiederkehrende Formate, Geschichten, die euer Publikum erkennt und wieder sehen will. Deshalb startet jede Produktion bei uns mit einem Workshop, in dem wir genau das mit euch erarbeiten.
**Support Text EN:** _(leer)_

#### 4. `magazine-manifest`
_(block-id: 69fca1b2a8642ed6214c6e1f)_

**Eyebrow DE:** Wie wir produzieren.
**Eyebrow EN:** _(leer)_
**Sub-Headline DE:** Regelmäßige Produktion statt einzelner Drehs.
**Sub-Headline EN:** _(leer)_
**Lead DE:** Wir produzieren Reels & Stories Content nicht als einzelnes Projekt. Wir bauen mit euch eine laufende Produktions-Routine, die jeden Monat verlässlich Inhalte hervorbringt.
**Lead EN:** _(leer)_
**Body DE:**
> Nach dem Workshop wisst ihr, welche Geschichten ihr erzählen wollt. Was dann fehlt, ist die Produktions-Maschine, die diese Geschichten konsistent in fertige Inhalte verwandelt. Genau dort setzen wir an.
> Jeder Monat startet mit einem Planungscall, in dem wir Schwerpunkte und Themen festlegen. Daraus entstehen Shooting Scripts, Drehpläne, Shot-Listen. Am Drehtag setzen wir das gemeinsam um, schneiden im Anschluss, und übergeben fertige Files. Was wir dabei produzieren, baut auf eurem Storytelling Guide aus dem Workshop auf, sodass jeder neue Reel einen klaren Platz in eurer Marken-Erzählung hat.
> Zwei Dinge unterscheiden uns von klassischen Social-Media-Agenturen. Erstens denken wir filmisch: wir kommen aus zwölf Jahren Markenfilm und übersetzen diese Tiefe in 30-Sekunden-Formate. Zweitens sind wir modular: ihr nutzt nur die Bausteine, die ihr braucht. Drehtag und Schnitt von uns, Posting selbst? Eine Agentur kümmert sich um Redaktion? Ihr dreht selbst und liefert nur Rohmaterial? Alles möglich.

**Body EN:**
_(leer)_

##### Pull Quote
**Quote DE:** _(leer)_
**Quote EN:** _(leer)_

#### 5. `process-timeline`
_(block-id: 69fca5460862b1bb4e31be63)_

**Section Eyebrow DE:** Laufende Produktion.
**Section Eyebrow EN:** _(leer)_
**Section Headline DE:** So läuft jeder Monat ab.
**Section Headline EN:** _(leer)_
**Section Intro DE:** Vier Bausteine, in einer Schleife. Welche Bausteine ihr nutzt und welche ihr selbst oder mit eurer Agentur abdeckt, entscheidet ihr.
**Section Intro EN:** _(leer)_

##### Step 1
**Label DE:** Phase 01
**Label EN:** _(leer)_
**Title DE:** Konzept & Drehplanung
**Title EN:** _(leer)_
**Pricing DE:** ab 500 € / Monat
**Pricing EN:** _(leer)_
**Description DE:** 1-stündiger Planungscall pro Monat. Wir schmieden den Plan: Themen-Schwerpunkte, konkrete Inhalts-Vorschläge, Shooting Scripts, Shot-Listen, Drehplan inkl. Location und Crew.
**Description EN:** _(leer)_

##### Step 2
**Label DE:** Phase 02
**Label EN:** _(leer)_
**Title DE:** Drehtag Small
**Title EN:** _(leer)_
**Pricing DE:** ab 900 € / Tag
**Pricing EN:** _(leer)_
**Description DE:** 8 Stunden Drehtag mit Kamera, Ton und kleinem Lichtpaket. Aus einem Drehtag entstehen typischerweise 5-12 fertige Clips. Oder auch aufgeteilt auf zwei Halbtage. Spezialequipment auf Anfrage, im Grunde ist alles möglich.
**Description EN:** _(leer)_

##### Step 3
**Label DE:** Phase 03
**Label EN:** _(leer)_
**Title DE:** Postproduktion
**Title EN:** _(leer)_
**Pricing DE:** ab 800€ / Tag · 75€-150€ / Film
**Pricing EN:** _(leer)_
**Description DE:** Schnitt der gedrehten Inhalte. Bei Drehtag-Setups ab 800€ / Tag. Wenn ihr selbst dreht und uns das Material schickt: 75 - 150 € pro Film, je nach Komplexität.
**Description EN:** _(leer)_

##### Step 4 (Optional)
**Label DE:** Phase 04
**Label EN:** _(leer)_
**Title DE:** Social Media Betreuung
**Title EN:** _(leer)_
**Pricing DE:** ab 450€ / Monat
**Pricing EN:** _(leer)_
**Description DE:** Redaktionsplan der von von uns produzierten Inhalte, Texte, Freigabeprozesse, Posting. Optional, viele Marken decken das selbst oder über ihre Agentur ab.
**Description EN:** _(leer)_

**Footnote DE:** Konkrete Konfiguration und Kombinationen besprechen wir im Erstgespräch.
**Footnote EN:** _(leer)_

#### 6. `magazine-manifest`
_(block-id: 69fca291a8642ed6214c6e21)_

**Eyebrow DE:** Wie Kunden mit uns arbeiten.
**Eyebrow EN:** _(leer)_
**Sub-Headline DE:** Viele Wege führen zum Content.
**Sub-Headline EN:** _(leer)_
**Lead DE:** Die Bausteine sind modular. In der Praxis sehen die häufigsten Konstellationen so aus.
**Lead EN:** _(leer)_
**Body DE:**
„Aus einer Hand" - Wir konzipieren monatlich, drehen mit unserem Team, schneiden, übergeben fertige Files. Ihr postet, oder eure Agentur. Setup für Unternehmen, die internes Volumen nicht aufbauen wollen.
„Wir denken und schneiden, ihr dreht" - Ihr habt einen Videograph oder dreht selbst. Wir liefern Konzeption, Scripts, Shot-Listen, später schneiden wir aus eurem Material. Gut für Marken mit eigenem Setup.
„Nur Konzeption" - Monatliche Scripts und Drehpläne, sonst nichts. Ihr setzt um, ihr schneidet, ihr postet. Für Marken mit voll funktionierendem internen Setup, die ihrer Produktion mehr Storytelling-Tiefe geben wollen.
„Ergänzung zur Agentur" - Ihr habt eine Social-Media-Agentur, die euer Posting macht. Wir steuern Konzeption und Premium-Drehtag bei, eure Agentur ergänzt mit Plan und Posting.
Das sind nur vier Beispiele. In der Praxis baut jedes Setup auf eurer Situation auf: was ihr habt, was ihr braucht, was ihr selbst tragen wollt.

**Body EN:**
_(leer)_

##### Pull Quote
**Quote DE:** Wir bauen den Workflow um eure Realität herum. Nicht andersherum.
**Quote EN:** _(leer)_

#### 7. `testimonials`
_(block-id: 69fca329a8642ed6214c6e23)_

**Headline DE:** _(leer)_
**Headline EN:** _(leer)_
_Filter: area=rs · onlyFeatured=True_

#### 8. `faq`
_(block-id: 69fca34ca8642ed6214c6e25)_

**Eyebrow DE:** Klartext.
**Eyebrow EN:** _(leer)_
**Headline DE:** Was uns oft gefragt wird.
**Headline EN:** _(leer)_

##### FAQ 1
**Question DE:** Müssen wir vor Production-Start einen Workshop machen?
**Question EN:** _(leer)_
**Answer DE:**
Empfohlen, weil Produktion ohne Strategie schnell wirkungslos wird. Wenn ihr aber bereits ein klares Storytelling-Konzept und definierte Formate habt, können wir auch direkt einsteigen. Im Erstgespräch wird klar, welcher Weg sinnvoll ist.

**Answer EN:**
_(leer)_

##### FAQ 2
**Question DE:** Können wir nur einzelne Bausteine bei euch buchen?
**Question EN:** _(leer)_
**Answer DE:**
Ja. Drehtag plus Schnitt nur für ein Projekt? Oder nur monatliche Konzeption? Beides geht. Die Bausteine sind so geschnitten, dass sie einzeln Sinn machen und in Kombination skalieren.

**Answer EN:**
_(leer)_

##### FAQ 3
**Question DE:** Wir haben schon eine Social-Media-Agentur. Konkurriert ihr mit ihr?
**Question EN:** _(leer)_
**Answer DE:**
Nein. Wir füllen die Lücken mit unserer Expertise: Storytelling-Tiefe und filmische Premium-Produktion. Eure Agentur kümmert sich weiter um Redaktion und Posting, wir liefern die kreativen und filmischen Bausteine. Das hat schon mehrfach gut funktioniert.

**Answer EN:**
_(leer)_

##### FAQ 4
**Question DE:** Wie sieht ein typischer Drehtag aus?
**Question EN:** _(leer)_
**Answer DE:**
8 Stunden vor Ort, mit Kamera, Ton und kleinem Lichtpaket. Wir folgen dem Drehplan aus der Konzeption. Aus einem Drehtag entstehen typischerweise 5-12 fertige Clips, je nach Komplexität und Wechsel-Aufwand zwischen Settings. Oder zwei Halb-Tage weil das besser in euren Ablauf passt, wir sind flexibel.

**Answer EN:**
_(leer)_

##### FAQ 5
**Question DE:** Wie schnell sind die ersten Filme da?
**Question EN:** _(leer)_
**Answer DE:**
Erstgespräch und Workshop in zwei bis drei Wochen, erste Konzeption und Drehplanung im Folgemonat, erster Drehtag dann meist im Monat danach. Nach dem Setup laufen die Zyklen monatlich verlässlich.

**Answer EN:**
_(leer)_

##### FAQ 6
**Question DE:** Was ist der Unterschied zu einer klassischen Werbefilm-Produktion?
**Question EN:** _(leer)_
**Answer DE:**
Eine Werbefilm-Produktion ist auf einen Schuss ausgelegt: ein Konzept, ein Dreh, ein fertiger Spot. Reels & Stories Content-Produktion erfolgt regelmäßig: monatlicher Zyklus, modular, auf eine Marken-Erzählung ausgelegt, die über Monate trägt. Andere Disziplin, anderer Output.

**Answer EN:**
_(leer)_

##### FAQ 7
**Question DE:** Welche Plattformen produzieren wir?
**Question EN:** _(leer)_
**Answer DE:**
Vertikales und 4:5-Bewegtbild, wenn nötig auch Querformat. Primär Instagram, TikTok, LinkedIn. YouTube für Evergreen-Formate. Welche Plattformen für eure Marke wirklich Sinn machen, klären wir im Workshop oder im Erstgespräch.

**Answer EN:**
_(leer)_

#### 9. `cta`
_(block-id: 69fca44da8642ed6214c6e35)_

**Headline DE:** Lasst uns über euren Workflow reden.
**Headline EN:** _(leer)_
**Subline DE:** 30 Minuten Erstgespräch, ohne Rechnung. Wir hören uns an, was ihr produzieren wollt und welche Bausteine bei euch Sinn machen.
**Subline EN:** _(leer)_
_Variant: form_

---

#### SEO

**Meta Title DE:** _(leer)_
**Meta Title EN:** _(leer)_

**Meta Description DE:** _(leer)_
**Meta Description EN:** _(leer)_

---

### 19. Reels & Stories Workshop

- **ID:** 13
- **URL-Path:** `/reels-stories/workshop`
- **Slug:** `workshop`
- **Area:** rs
- **Visibility:** public

**Title DE:** Reels & Stories Workshop
**Title EN:** _(leer)_

#### Sections (11)

#### 1. `hero`
_(block-id: 69f5054e4fde8d096c482505)_

_Variant: landing_

**Headline DE:** _(leer)_
**Headline EN:** _(leer)_
**Subline DE:** _(leer)_
**Subline EN:** _(leer)_

#### 2. `bold-statement`
_(block-id: 69fc7c76845c877b229b7c3e)_

**Line 1 DE:** Vom Posten
**Line 1 EN:** _(leer)_
**Line 2 (Copper) DE:** zur Marke.
**Line 2 (Copper) EN:** _(leer)_
**Tagline DE:** Der Workshop für Unternehmen, die mehr sein wollen als ein Profil.
**Tagline EN:** _(leer)_

#### 3. `problem-statement`
_(block-id: 69fc7c85845c877b229b7c40)_

**Eyebrow DE:** Ehrlich gesagt.
**Eyebrow EN:** _(leer)_
**Headline DE:** Posten ohne Plan ist Beschäftigungstherapie.
**Headline EN:** _(leer)_
**Support Text DE:** Viele Unternehmen und Einzelunternehmer:innen posten täglich, ohne zu wissen warum. Reichweite wird zur Suchaufgabe statt zur Folge. Algorithmus-Hacks und Posting-Frequenz lösen nicht das eigentliche Problem: ohne einen Kern, der trägt, ist jeder Posting-Plan nur ein Plan ohne Substanz. Bevor ihr mehr postet, lohnt es sich, zu klären, was euer Unternehmen wirklich auszeichnet. Das ist der erste Schritt von „Profil" zu „Marke".
**Support Text EN:** _(leer)_

#### 4. `magazine-manifest`
_(block-id: 69fc8812845c877b229b7c42)_

**Eyebrow DE:** Was uns unterscheidet
**Eyebrow EN:** _(leer)_
**Sub-Headline DE:** Wir arbeiten am Fundament, nicht am Frequenzplan.
**Sub-Headline EN:** _(leer)_
**Lead DE:** Der Reels & Stories Workshop ist ein Format-Workshop. Wir helfen Unternehmen und Einzelunternehmer:innen, ihre Marke zu finden - nicht den nächsten Posting-Plan zu schreiben.
**Lead EN:** _(leer)_
**Body DE:**
Andere Workshops trainieren euch im Umgang mit Algorithmen, Frequenz und Tactics. Wir setzen davor an. In den zwei bis drei Stunden, die wir miteinander verbringen, arbeiten wir an den drei Säulen, auf denen euer Content stehen muss: was euch ausmacht, wo eure Substanz liegt, und welche Beweise eure Geschichten tragen können.
Wir kommen vorbereitet. Vor dem Workshop recherchieren wir eure Marke und euer Marktumfeld. Wir bringen ein Framework, konkrete Fragen und einen klaren Plan für das Gespräch mit. Es ist keine Brainstorming-Session, in der ihr selbst die Hälfte denken müsst. Wir leiten und verdichten gemeinsam mit euch.

**Body EN:**
_(leer)_

##### Pull Quote
**Quote DE:** Wer Reichweite ohne Substanz baut, baut ein Megaphon ohne Stimme.
**Quote EN:** _(leer)_

#### 5. `services-grid`
_(block-id: 69fc8883845c877b229b7c44)_

**Eyebrow DE:** Ablauf.
**Eyebrow EN:** _(leer)_
**Headline DE:** So läuft der Workshop ab.
**Headline EN:** _(leer)_
**Intro DE:** _(leer)_
**Intro EN:** _(leer)_

##### Service 1
**Eyebrow DE:** Vorbereitung.
**Eyebrow EN:** _(leer)_
**Title DE:** Wir kommen vorbereitet.
**Title EN:** _(leer)_
**Description DE:** Vor dem Termin recherchieren wir eure Marke, eure bisherige Kommunikation und euer Marktumfeld - im Idealfall mit Analysedaten eurer Plattformen. Wir bringen ein Framework, konkrete Fragen und Gesprächsleitung mit. Ihr müsst nichts vorbereiten - außer offen sein.
**Description EN:** _(leer)_

##### Service 2
**Eyebrow DE:** Workshop.
**Eyebrow EN:** _(leer)_
**Title DE:** 2-3 Stunden vor Ort.
**Title EN:** _(leer)_
**Description DE:** Strukturiertes Gespräch entlang eines Leitfadens. Wir leiten, stellen Fragen und hören zu. Ihr antwortet, wir verdichten gemeinsam. Keine Brainstorming-Session, in der ihr selbst die Hälfte denken müsst.
**Description EN:** _(leer)_

##### Service 3
**Eyebrow DE:** Storytelling Guide.
**Eyebrow EN:** _(leer)_
**Title DE:** Wir verarbeiten und gestalten.
**Title EN:** _(leer)_
**Description DE:** Im Anschluss arbeiten wir intern weiter. Wir entwickeln einen Social Media Storytelling Guide, der eure drei Säulen, eure Formate und eure Produktions-Logik dokumentiert. Individuell für eure Marke, kein Template.
**Description EN:** _(leer)_

##### Service 4
**Eyebrow DE:** Handoff.
**Eyebrow EN:** _(leer)_
**Title DE:** Präsentation und Übergabe.
**Title EN:** _(leer)_
**Description DE:** Wir präsentieren den Guide gemeinsam, klären offene Fragen, bauen euer Feedback ein und übergeben das finale Dokument. Was ihr danach in der Hand habt: einen Plan, mit dem ihr eigenständig produzieren könnt - oder gemeinsam mit uns weiterarbeitet.
**Description EN:** _(leer)_

#### 6. `partnership-block`
_(block-id: 69fc928f845c877b229b7c7c)_

**Eyebrow DE:** Methodik.
**Eyebrow EN:** _(leer)_
**Headline DE:** Drei Säulen. Pro Säule drei Formate.
**Headline EN:** _(leer)_

##### Pillar 1
**Eyebrow DE:** Säule 01 · Identifikation
**Eyebrow EN:** _(leer)_
**Headline DE:** Wer ihr seid.
**Headline EN:** _(leer)_
**Body DE:**
_(leer)_

**Body EN:**
_(leer)_

##### Pillar 2
**Eyebrow DE:** Säule 02 · Expertise
**Eyebrow EN:** _(leer)_
**Headline DE:** Was ihr wisst.
**Headline EN:** _(leer)_
**Body DE:**
_(leer)_

**Body EN:**
_(leer)_

##### Pillar 3
**Eyebrow DE:** Säule 03 · Beweis
**Eyebrow EN:** _(leer)_
**Headline DE:** Was ihr macht.
**Headline EN:** _(leer)_
**Body DE:**
_(leer)_

**Body EN:**
_(leer)_

#### 7. `magazine-manifest`
_(block-id: 69fc8a3d845c877b229b7c58)_

**Eyebrow DE:** Was ihr in der Hand habt.
**Eyebrow EN:** _(leer)_
**Sub-Headline DE:** Der Social Media Storytelling Guide.
**Sub-Headline EN:** _(leer)_
**Lead DE:** Nach dem Workshop bekommt ihr keinen netten Foliensatz. Ihr bekommt euer Playbook.
**Lead EN:** _(leer)_
**Body DE:**
Der Guide ist das physische Outcome des Workshops. Individuell für eure Marke, basierend auf dem, was im Workshop entstanden ist. Er dokumentiert eure drei Säulen, eure neun Formate, eure Produktions-Logik und konkrete Beispiele für die ersten Drehs.
Mit diesem Dokument habt ihr alles in der Hand, was ihr braucht. Ihr könnt selbst weiterproduzieren, einen Videographen briefen, oder mit uns gemeinsam in die Produktion gehen. Es ist kein Template-Generator, sondern eure eigene Marken-Bedienungsanleitung. Auch externe Partner können damit arbeiten, ohne dass eure Stimme verwässert.

**Body EN:**
_(leer)_

##### Pull Quote
**Quote DE:** Mit dem Guide könnt ihr selbst produzieren. Müsst aber nicht.
**Quote EN:** _(leer)_

#### 8. `pricing-tiers`
_(block-id: 69fc8acc845c877b229b7c5a)_

**Section Eyebrow DE:** Aktuell verfügbar.
**Section Eyebrow EN:** _(leer)_
**Section Headline DE:** Was der Workshop kostet.
**Section Headline EN:** _(leer)_
**Section Intro DE:** Aktuell als ein Format buchbar. Tiefer-gehende Workshop-Stufen entwickeln wir gerade.
**Section Intro EN:** _(leer)_

##### Tier 1
**Eyebrow DE:** _(leer)_
**Eyebrow EN:** _(leer)_
**Name DE:** Reels & Stories Workshop
**Name EN:** _(leer)_
_Price (lang-neutral): 1.500€_
**Price Unit DE:** einmalig
**Price Unit EN:** _(leer)_
**Description DE:** Vorbereitung, 2-3 Stunden Workshop vor Ort, Storytelling Guide und Übergabe-Termin.
**Description EN:** _(leer)_
**Includes Item 1 DE:** Vorab-Recherche eurer Marke und bisherigen Kommunikation auf Basis von Analysedaten
**Includes Item 1 EN:** _(leer)_
**Includes Item 2 DE:** 2-3 Stunden Workshop vor Ort, von uns geleitet
**Includes Item 2 EN:** _(leer)_
**Includes Item 3 DE:** Individueller Social Media Storytelling Guide
**Includes Item 3 EN:** _(leer)_
**Includes Item 4 DE:** Präsentations- und Feedback-Termin
**Includes Item 4 EN:** _(leer)_
**Includes Item 5 DE:** Finaler Handoff des Guides
**Includes Item 5 EN:** _(leer)_
**CTA Label DE:** Lass uns reden
**CTA Label EN:** _(leer)_

##### Tier 2
**Eyebrow DE:** _(leer)_
**Eyebrow EN:** _(leer)_
**Name DE:** Workshop + Produktion
**Name EN:** _(leer)_
_Price (lang-neutral): 950€_
**Price Unit DE:** einmalig
**Price Unit EN:** _(leer)_
**Description DE:** Reduzierter Workshop-Preis, wenn ihr direkt mit uns produziert. Zwei Wege: ein einmaliger Drehtag, um eure Formate professionell aufzusetzen, oder ein flexibel-individuelles Content-Abo für laufende Produktion.
**Description EN:** _(leer)_
**Includes Item 1 DE:** Alles aus „Workshop Solo": Vorbereitung, Workshop, Guide, Übergabe
**Includes Item 1 EN:** _(leer)_
**Includes Item 2 DE:** Entweder: Drehtag zum professionellen Format-Setup
**Includes Item 2 EN:** _(leer)_
**Includes Item 3 DE:** Oder: flexibel-individuelles Content-Abo
**Includes Item 3 EN:** _(leer)_
**Includes Item 4 DE:** Konkretes Pricing eurer Produktion im Erstgespräch
**Includes Item 4 EN:** _(leer)_
**CTA Label DE:** Lass uns reden
**CTA Label EN:** _(leer)_

**Footnote DE:** Welcher Weg zu eurem Setup passt und was eure Production konkret kostet, klären wir im Erstgespräch.
**Footnote EN:** _(leer)_

#### 9. `testimonials`
_(block-id: 69fc8b7b845c877b229b7c68)_

**Headline DE:** _(leer)_
**Headline EN:** _(leer)_
_Filter: area=rs · onlyFeatured=False_

#### 10. `faq`
_(block-id: 69fc8bab845c877b229b7c6a)_

**Eyebrow DE:** Klartext.
**Eyebrow EN:** _(leer)_
**Headline DE:** Was uns oft gefragt wird.
**Headline EN:** _(leer)_

##### FAQ 1
**Question DE:** Was unterscheidet diesen Workshop von einem Social-Media-Strategie-Workshop?
**Question EN:** _(leer)_
**Answer DE:**
> Eine Social-Media-Strategie sagt euch, welche Plattformen ihr bedienen sollt und in welcher Frequenz. Unser Workshop beantwortet die Frage davor: welche Geschichten ihr dort erzählen sollt und wie. Die zwei ergänzen sich, ersetzen sich aber nicht. Wenn ihr noch keinen narrativen Kern habt, helfen euch Algorithmus-Tipps wenig.

**Answer EN:**
_(leer)_

##### FAQ 2
**Question DE:** Wie lange dauert der Workshop?
**Question EN:** _(leer)_
**Answer DE:**
Der Workshop selbst ist auf 2-3 Stunden vor Ort ausgelegt. Davor läuft unsere Vorbereitung (Recherche eurer Marke und Kommunikation auf Basis von Analysedaten), danach folgt die interne Verarbeitung, eine Präsentation des Guides und der finale Handoff. Vom Workshop-Termin bis zum übergebenen Guide vergehen typischerweise zwei bis drei Wochen.

**Answer EN:**
_(leer)_

##### FAQ 3
**Question DE:** Was ist im Storytelling Guide enthalten?
**Question EN:** _(leer)_
**Answer DE:**
> Der Guide dokumentiert euren narrativen Kern, die drei Säulen, die neun Formate, die Produktions-Logik und konkrete Beispiele für eure ersten Drehs. Er ist zugeschneidert für euch, kein Template. Mit ihm könnt ihr selbst weiterproduzieren oder einen externen Partner briefen, ohne dass eure Stimme verwässert.

**Answer EN:**
_(leer)_

##### FAQ 4
**Question DE:** Müssen wir auf etwas vorbereitet sein?
**Question EN:** _(leer)_
**Answer DE:**
Nein. Wir leiten den Workshop mit Framework und Fragen, ihr müsst nicht vorbereiten denn ihr wisst bereits alles über euch und eure Marke, wir müssen es nur ans Licht bringen. Hilfreich ist es, wenn die Personen am Tisch sind, die später produzieren oder Entscheidungen über die Kommunikation treffen. Optional ist es sehr hilfreich Analysedaten eurer Social Media Plattformen zu exportieren.

**Answer EN:**
_(leer)_

##### FAQ 5
**Question DE:** Wer sollte am Workshop teilnehmen?
**Question EN:** _(leer)_
**Answer DE:**
Mindestens die Geschäftsführung oder Eigentümer:in (wer die Marke trägt). Bei Teams: zusätzlich die Personen, die später produzieren oder die Inhalte verantworten. Mehr als vier bis fünf Personen sprengen den Rahmen.

**Answer EN:**
_(leer)_

##### FAQ 6
**Question DE:** Was passiert nach dem Workshop?
**Question EN:** _(leer)_
**Answer DE:**
Ihr entscheidet. Mit dem Guide könnt ihr selbst produzieren, einen Videograph briefen, oder mit uns weiterarbeiten. Wir kombinieren die Bausteine - Drehplanung, Drehtag, Postproduction, Posting - so, wie es zu eurer Realität passt. Nur den Workshop machen ist auch in Ordnung.

**Answer EN:**
_(leer)_

##### FAQ 7
**Question DE:** Bietet ihr den Workshop auch online an?
**Question EN:** _(leer)_
**Answer DE:**
Ja, es ist auch per Video Call möglich, wichtig ist nur eine gute Sprachverbindung. Wenn irgend möglich ist ein Workshop vor Ort allerdings oftmals ein netterer Rahmen für ein persönliches Gespräch.

**Answer EN:**
_(leer)_

#### 11. `cta`
_(block-id: 69fc8d6e845c877b229b7c7a)_

**Headline DE:** Lass uns reden.
**Headline EN:** _(leer)_
**Subline DE:** 30 Minuten Erstgespräch, ohne Rechnung. Wir hören uns an, wo ihr steht und was ihr braucht. Daraus wird klar, ob unser Workshop für euch passt.
**Subline EN:** _(leer)_
_Variant: form_

---

#### SEO

**Meta Title DE:** _(leer)_
**Meta Title EN:** _(leer)_

**Meta Description DE:** _(leer)_
**Meta Description EN:** _(leer)_

---
