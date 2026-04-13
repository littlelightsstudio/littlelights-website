# CEO Strategie Artifact: Konzept
**Interaktives HTML-Dokument für wöchentliche, monatliche und quartalsweise Reviews | April 2026**

---

## Zweck

Ein visuelles, interaktives HTML-Dokument (Claude Chat Artifact), das Michael durch drei Rhythmen führt:
- **Weekly:** Persönlicher CEO Check-in (15-20 min, mit Claude)
- **Monthly:** Team-Meeting-Vorbereitung (wird dann auch dem Team präsentiert)
- **Quarterly:** Strategie-Review (tiefere Analyse, Kurskorrektur)

Das CEO-Artifact ist ein **privates Arbeits- und Entscheidungsdokument**. Für Team-Meetings wird ein separates, reduziertes Dokument generiert, das nur die teamrelevanten Informationen enthält. Kein Präsentations-Toggle, sondern zwei getrennte Outputs, um sensible Überlegungen zu schützen.

---

## Design-Prinzipien

- Gleicher Stil wie Arthur Real Storytelling Guide (Satoshi, Kartenbasiert, heller Hintergrund)
- Kein Präsentations-Toggle. CEO-Artifact ist privat. Team-Meeting-Output wird separat generiert.
- Mobile-first (wird am Handy und Tablet genutzt)
- Claude Chat befüllt das Artifact mit aktuellen Daten aus Notion
- Farbcodes für Status: Grün (on track), Orange (Aufmerksamkeit), Rot (at risk), Grau (geparkt)

---

## Struktur

### Header

```
LITTLE LIGHTS STUDIO                    [Woche 15 · April 2026]
CEO Strategie Dashboard                  [Weekly | Monthly | Quarterly]
```

Tab-Navigation: Weekly / Monthly / Quarterly (je nach aktuellem Bedarf)

---

### Tab 1: WEEKLY (wöchentlicher CEO Check-in)

**Ziel:** In 15 Minuten wissen wo alles steht und was diese Woche zählt.

#### Sektion 1: Wochenfokus
Karte mit den 3 wichtigsten Prioritäten dieser Woche.
- Was ist der eine Hebel, der diese Woche den größten Unterschied macht?
- Was darf NICHT liegen bleiben?
- Was kann warten?

#### Sektion 2: Firmenprojekte Status
Kompakte Karten pro internem Projekt, jeweils:

```
[Status-Farbe]  Projektname
                Einzeiler: Was ist der aktuelle Stand?
                Nächster Schritt: Was steht als nächstes an?
                Blocker: (nur wenn vorhanden)
```

Projekte:
- Website Redesign
- Reels & Stories Aufbau
- Neukundenakquise Agency
- Eigene Social Media Präsenz
- Finanzen & Controlling
- Publishing (Trilogie)
- [weitere nach Bedarf]

#### Sektion 3: Pipeline & Umsatz
- Offene Angebote / Pitches (Name, Volumen, Wahrscheinlichkeit)
- Bestätigte Projekte diesen Monat
- Umsatz-Tracking vs. Ziel (wenn vorhanden)

#### Sektion 4: Entscheidungen
- Was steht diese Woche an, das entschieden werden muss?
- Aufgeschobene Entscheidungen (seit wann offen?)

#### Sektion 5: Follow Ups
- Wichtige Follow-Ups die nicht vergessen werden dürfen
- Überfällige Follow-Ups (rot markiert)

---

### Tab 2: MONTHLY (Team-Meeting-Vorbereitung)

**Ziel:** Monatlichen Überblick haben, Team-Meeting vorbereiten, Kurskorrektur wenn nötig.

#### Sektion 1: Monatsüberblick
- Was waren die Highlights diesen Monat?
- Was lief nicht wie geplant?
- 2-3 Sätze Zusammenfassung

#### Sektion 2: Strategische Ziele Status
Aus der Notion Strategie & Ziele DB:
```
[Status-Icon]  Zielname
               Fokus: Now / Next / Later
               Fortschritt: X von Y Milestones
               Verantwortlich: Name
               Nächster Milestone: ...
```

#### Sektion 3: Finanzüberblick
- Umsatz Monat vs. Plan
- Offene Rechnungen
- Cashflow-Tendenz
- Kritische Posten

#### Sektion 4: Teamkapazität
- Wer ist überlastet?
- Wer hat Kapazität?
- Engpässe

#### Sektion 5: Nächster Monat
- Top 3 Prioritäten
- Anstehende Deadlines
- Entscheidungen die getroffen werden müssen

#### Sektion 6: Team-Meeting Agenda (auto-generiert)
- Highlights & Wins
- Herausforderungen
- Strategische Ziele Update
- Nächste Schritte
- Offene Fragen

---

### Tab 3: QUARTERLY (Strategie-Review)

**Ziel:** Tiefer Blick auf die Strategie. Kurskorrektur. Ziele für nächstes Quartal.

#### Sektion 1: Quartalszusammenfassung
- Was haben wir erreicht?
- Was haben wir nicht geschafft?
- Was hat sich verändert (Markt, Kunden, Team)?

#### Sektion 2: Ziele-Review
Jedes strategische Ziel einzeln:
- Status am Quartalsende
- Was war geplant vs. was ist passiert
- Weiterführen / Anpassen / Parken / Abschließen

#### Sektion 3: Finanzen Quartal
- Umsatz Q vs. Vorjahresquartal
- Kundenverteilung (Abhängigkeiten?)
- Wiederkehrender Umsatz (Reels & Stories)
- Prognose nächstes Quartal

#### Sektion 4: Team & Organisation
- Teamstruktur: funktioniert sie?
- Aufgabenverteilung: richtig?
- Was fehlt?

#### Sektion 5: Markt & Positionierung
- Neue Entwicklungen im Markt
- Konkurrenz-Update (wenn relevant)
- Positionierung: stimmt der Kurs?

#### Sektion 6: Nächstes Quartal
- Top 3 Ziele
- Meilensteine
- Entscheidungen

---

## Datenquellen

| Sektion | Quelle |
|---------|--------|
| Firmenprojekte | CEO Weekly Seite (Notion) |
| Strategische Ziele | Strategie & Ziele DB (Notion) |
| Pipeline | CRM DB (Notion) |
| Follow Ups | CRM / Dashboard (Notion) |
| Finanzen | CEO Weekly (Zusammenfassung aus Financial Dashboard Report) |
| Teamkapazität | Manueller Input |

---

## Workflow

### Weekly (jeden Montag oder Sonntagabend)
1. Michael öffnet Claude Chat
2. Claude liest CEO Weekly + Strategie DB aus Notion
3. Michael berichtet frei: "Diese Woche ist passiert / steht an..."
4. Michael teilt die Finanz-Zusammenfassung aus dem Financial Dashboard (Kennzahlen, Cashflow, kritische Posten)
5. Claude aktualisiert das Artifact und die CEO Weekly Notion-Seite (inkl. Finanz-Sektion)
6. Dauer: 15-20 Minuten

### Monthly (letzter Freitag im Monat)
1. Michael öffnet Claude Chat
2. Claude liest alle Notion-Quellen, fasst den Monat zusammen
3. Michael ergänzt/korrigiert
4. Claude generiert Monthly-Tab als Präsentation UND Team-Meeting-Agenda
5. Michael nutzt das Artifact im Team-Meeting (Präsentations-Modus)
6. Dauer: 30-45 Minuten Vorbereitung

### Quarterly (letzter Freitag im Quartal)
1. Wie Monthly, aber tiefer
2. Claude zieht die letzten 3 Monthly-Zusammenfassungen heran
3. Strategie-Review, Ziele-Anpassung
4. Ergebnis: Ziele und Meilensteine für nächstes Quartal werden in Notion aktualisiert
5. Dauer: 60-90 Minuten

---

## Technische Umsetzung

- Single-page HTML, optimiert für Claude Chat Artifacts
- Satoshi Font, Farbschema wie Arthur Real Guide
- Tab-Navigation (Weekly/Monthly/Quarterly)
- Präsentations-Toggle (kompakt vs. Detail)
- Kein externer Datenabruf im HTML selbst (Claude befüllt es)
- Responsive: Mobile, Tablet, Desktop

**Umsetzung in einer dedizierten Claude Chat Session.** Dieses Konzept dient als Briefing.
