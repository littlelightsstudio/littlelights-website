# KI-Inventar Little Lights Studio

Übersicht aller eingesetzten KI-Tools, Datenflüsse und Compliance-Status. Lebendes Dokument: bei jeder Tool-Änderung (neuer Anbieter, neuer Sub-Processor, geänderte AGB) hier nachziehen.

**Letztes Review:** 2026-05-04
**Nächstes geplantes Review:** 2026-08-04 (quartalsweise)
**Verantwortlich:** Michael Sokolar

---

## Erfasste Tools

### Anthropic Claude

| Aspekt | Details |
|---|---|
| **Anbieter** | Anthropic, San Francisco, USA |
| **Produkte im Einsatz** | Claude Code (CLI), Claude.ai (Chat), Claude in CoWork-Workflows |
| **Zweck** | Code-Entwicklung, Recherche, Texterstellung-Assistenz, Konzeption, Skript-Drafts |
| **Datenkategorien** | Code, Texte, ggf. Kunden-Briefings (sofern hochgeladen) |
| **Personenbezogene Daten** | In der Regel nein. Falls ausnahmsweise (z.B. Briefing mit Klarnamen): nur über Claude.ai-Konten ohne Trainings-Zustimmung oder per API |
| **Datenstandort** | USA (mit EU-Standardvertragsklauseln) |
| **Trainings-Daten-Nutzung** | API: standardmäßig nein. Claude.ai: opt-out in Settings, muss sichergestellt sein |
| **DPA / AVV** | Anthropic Commercial Terms inkl. Data Processing Addendum verfügbar |
| **Sub-Processors** | AWS, Google Cloud (US-Rechenzentren) |
| **Status** | ✅ Aktiv |
| **Risiko-Klasse (AI Act)** | Minimal / Limited Risk |

### ElevenLabs

| Aspekt | Details |
|---|---|
| **Anbieter** | ElevenLabs Inc., USA |
| **Zweck** | Voiceover-Synthese, Voice-Cloning für Produktion |
| **Einsatz-Pattern** | Selektiv von Projekt zu Projekt. Bei finalen Produkten **nur wenn explizit ausgewiesen** |
| **Datenkategorien** | Sprachsamples (eigene oder mit Einwilligung Dritter), Skript-Texte |
| **Personenbezogene Daten** | Ja, sobald Stimmsamples realer Personen verarbeitet werden (biometrisches Datum) |
| **Einwilligungs-Pflicht** | Ja: ausdrückliche schriftliche Einwilligung jeder Stimme, deren Sample verarbeitet wird |
| **Datenstandort** | USA (mit Standardvertragsklauseln) |
| **DPA / AVV** | Verfügbar, muss pro Account abgeschlossen werden |
| **Status** | ✅ Aktiv (selektiv) |
| **Risiko-Klasse (AI Act)** | Limited Risk (Synthese-Audio, deepfake-fähig → Kennzeichnungspflicht bei finalem Output) |

### Generative KI für Bild/Video (Sammelposten)

> ⚠️ **Konkrete Tools hier eintragen** sobald klar welche im Einsatz sind. Kandidaten basierend auf Studio-Praxis:
> - Midjourney (Image Gen)
> - Adobe Firefly (Image Gen, integriert in Creative Cloud)
> - Sora (OpenAI)
> - Runway / Pika / Veo (Video Gen)

| Aspekt | Details |
|---|---|
| **Zweck** | Konzept-Visualisierung für Pitches, KI-gestützte Visuals in finalen Projekten (nur ausgewiesen) |
| **Einsatz-Pattern** | **Pitches:** Häufig, intern/B2B, keine öffentliche Veröffentlichung der KI-Outputs. **Finale Projekte:** Nur wenn explizit ausgewiesen + Kunden-Einwilligung |
| **Datenkategorien** | Prompts, Reference-Bilder (in der Regel keine personenbezogenen Daten) |
| **Datenstandort** | Variiert je Anbieter (meist USA) |
| **DPA-Status** | Pro Tool zu prüfen und hier ergänzen |
| **Status** | ✅ Aktiv |
| **Risiko-Klasse (AI Act)** | Limited Risk (Synthese-Inhalte → Kennzeichnungspflicht bei finalem Output) |

### Adobe (Creative Cloud + Firefly)

| Aspekt | Details |
|---|---|
| **Anbieter** | Adobe Inc., USA |
| **Produkte im Einsatz** | Premiere Pro, After Effects, Photoshop, Audition (lokal), ggf. Adobe Firefly (Cloud-AI) |
| **Zweck** | Standard-Postproduktion + KI-Funktionen (Generative Fill, Generative Expand, Audio-Enhance) |
| **Datenkategorien** | Projektdateien, Roh-Material |
| **Trainings-Daten-Nutzung** | Adobe-Cloud-Sync: Standard-Setting opt-out muss aktiv sein. Firefly: trainiert nur auf lizenzierten Beständen, keine Kunden-Inhalte |
| **Datenstandort** | USA (Adobe ist Data Privacy Framework zertifiziert) |
| **DPA / AVV** | Adobe Enterprise Terms inkl. DPA |
| **Status** | ✅ Aktiv |
| **Risiko-Klasse (AI Act)** | Minimal / Limited Risk je nach Funktion |

---

## Was nicht im Inventar ist (bewusst)

- Reine Office-AI-Features ohne Kunden-Daten-Bezug (z.B. Grammarly-Vorschläge, Mail-Autocomplete) sofern keine vertraulichen Inhalte verarbeitet werden
- Lokale ML-Features in Mac-OS (Spotlight, Diktieren etc.)

---

## Onboarding-Gate für neue Tools

Bevor ein neues KI-Tool im Studio produktiv eingesetzt wird:

1. In dieses Inventar eintragen (mindestens: Anbieter, Zweck, Datenkategorien, Datenstandort)
2. AGB / DPA prüfen, insbesondere:
   - Trainings-Daten-Klauseln (opt-out möglich?)
   - Datenstandort + Übermittlungs-Mechanismus
   - Sub-Processors
3. Einordnung in AI-Act-Risikoklasse
4. Falls Risiko-Klasse Limited oder höher → Hinweis in KI-Richtlinie ergänzen
5. Datenschutzerklärung der Website prüfen, ob Anbieter dort gelistet werden muss

---

## Quellen für Aktualität

- **Anbieter-Newsletter abonnieren:** Anthropic Trust Center, ElevenLabs Updates, Adobe Trust Center, OpenAI Privacy Updates
- **Compliance-Newsletter:** WKO Datenschutz-Updates, Stiftung Datenschutz
- **AI-Act-Specific:** Updates des [AI Office der EU-Kommission](https://digital-strategy.ec.europa.eu/en/policies/ai-office)
- **Quartals-Review** im Kalender als wiederkehrender Termin (4x/Jahr je 30 min)
