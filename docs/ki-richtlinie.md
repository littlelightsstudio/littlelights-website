# Interne KI-Richtlinie Little Lights Studio

Verbindliche Leitlinien für den Einsatz von KI-Tools in Studio-Projekten. Erfüllt die AI-Literacy-Anforderung des EU AI Act (Art. 4) und definiert den professionellen Umgang mit KI in Konzeption, Produktion und Auslieferung.

**Stand:** 2026-05-04
**Gültig für:** Alle Mitarbeitenden und freie Crew-Mitglieder von Little Lights Studio

---

## 1. Grundsätze

1. **KI ist Werkzeug, nicht Autor.** Die kreative und inhaltliche Verantwortung liegt immer bei den Menschen im Studio. KI unterstützt, ersetzt aber keine Konzeption, Regie oder Qualitätskontrolle.
2. **Transparenz nach außen.** Wenn KI substantiell zum finalen Werk beiträgt, wird das gegenüber Kunden und Publikum offengelegt.
3. **Vertraulichkeit nach innen.** Kunden-Materialien und sensible Informationen werden nur in Tools verarbeitet, die das vertraglich absichern.
4. **Aktualität.** Tool-Landschaft ändert sich schnell. Quartals-Review des Inventars ist Pflicht (siehe `ki-inventar.md`).

---

## 2. Erlaubte Tools

Verbindliche Liste: siehe [ki-inventar.md](./ki-inventar.md).

Vor Einsatz eines neuen Tools: Onboarding-Gate durchlaufen (siehe Inventar). Erst nach Eintrag ins Inventar darf produktiv gearbeitet werden.

---

## 3. Datenklassifizierung

Was darf in welche Tool-Kategorie?

| Datenklasse | Beispiele | Erlaubte Tools |
|---|---|---|
| **Öffentlich** | Bereits veröffentlichte Texte, eigene Brand-Assets, Stock-Material | Alle gelisteten Tools |
| **Intern** | Eigene Skript-Drafts, interne Notizen, Crew-Pläne | Alle gelisteten Tools |
| **Kunden-vertraulich** | Briefings, NDA-Material, unveröffentlichte Konzepte | Nur Tools mit DPA + opt-out vom Training (siehe Inventar). Im Zweifel: weglassen oder anonymisieren |
| **Personenbezogene Daten** | Klarnamen, Stimmsamples, Gesichter realer Personen | Nur mit ausdrücklicher schriftlicher Einwilligung der betroffenen Person + Tool mit DPA. Stimm-/Gesichts-Samples sind biometrische Daten (DSGVO Art. 9), strenger Schutz |

**Faustregel:** Wenn du nicht sicher bist, ob etwas in ein Tool darf — frag intern nach, bevor du paste machst.

---

## 4. Output-Review-Pflicht

Jeder KI-Output, der das Studio in Richtung Kunde oder Öffentlichkeit verlässt, durchläuft mindestens eine menschliche Review-Stufe:

- **Texte (Scripts, Konzepte, Mails):** Mindestens 1 Person liest gegen, prüft auf Halluzinationen, Faktentreue und Tonalität
- **Bild/Video:** Visuelle Prüfung auf typische KI-Artefakte (Hände, Augen, Geometrie, Logos), Markenrechte, Style-Treue
- **Audio:** Anhören auf Aussprache, Betonung, ungewollte Artefakte. Bei Voice-Cloning: Einwilligung der Stimm-Person dokumentiert

KI-Output **niemals direkt** an Kunden oder in finale Produkte ohne Review.

---

## 5. Kennzeichnungspflicht (EU AI Act, Art. 50)

### 5.1 Wann muss gekennzeichnet werden

Pflicht zur Kennzeichnung als KI-erstellt/manipuliert besteht bei:

- **Bild, Video, Audio**, das öffentlich gezeigt wird und realistisch wirkt (Deepfake-Definition)
- **Text**, der zur öffentlichen Information über Angelegenheiten von öffentlichem Interesse veröffentlicht wird

### 5.2 Wann nicht

- **Konzeption + Recherche** mit KI (Brainstorming, Skript-Drafts, Recherche-Assistenz): keine Kennzeichnungspflicht, da das finale Werk dann von Menschen gemacht wird
- **Pitches und interne Präsentationen:** in der Regel nicht öffentlich → keine AI-Act-Pflicht. **Aber:** dem Kunden gegenüber sollte transparent sein, dass Pitch-Visualisierungen KI-generiert sind und nicht das finale Produkt
- **Reine Postproduktion-Werkzeuge** ohne substantielle Inhalte-Generierung (z.B. Adobe Audio-Enhance, Color-Grading mit KI-Assistenz)

### 5.3 Wie kennzeichnen

- **Im Werk selbst:** sichtbarer Hinweis (Bauchbinde, Endcredit-Roll, Wasserzeichen, Caption)
- **Im Kontext:** Hinweis auf Projektseite der Website unter "KI-Einsatz"
- **Maschinenlesbar:** wenn das Tool Wasserzeichen / C2PA-Metadaten unterstützt → aktivieren

---

## 6. Pitches: Sonderfall

In Pitches setzen wir generative KI **frei** ein, um Konzepte zu visualisieren, ohne dafür schon Drehmaterial produzieren zu müssen. Regeln:

- **Keine Verwechslungsgefahr:** Dem Kunden gegenüber muss klar sein, dass Pitch-Visualisierungen KI sind, nicht das finale Werk. Standard-Disclaimer im Pitch-Deck: *"Visualisierungen mittels generativer KI. Finale Umsetzung erfolgt nach Briefing-Freigabe klassisch / hybrid / KI-gestützt (je nach Vereinbarung)."*
- **Keine Markenverletzungen:** Generierte Bilder dürfen keine geschützten Marken/Logos/Personen ohne Berechtigung enthalten
- **Pitch-Material ist nicht öffentlich:** wird nicht auf Website oder Social geteilt ohne explizite Freigabe + Kennzeichnung

---

## 7. Voice & Likeness

Bei jedem Einsatz von ElevenLabs oder ähnlichen Voice-Tools mit realer Stimme:

- **Schriftliche Einwilligung** der Stimm-Person vor Erstaufnahme. Template: siehe Studio-Vorlagen
- **Zweck-Bindung:** Einwilligung gilt nur für den vereinbarten Zweck (z.B. dieses Projekt). Nicht für künftige Reuse ohne neue Einwilligung
- **Widerrufsrecht** der betroffenen Person dokumentieren

Gleiches Prinzip gilt analog für Gesicht-Cloning / Likeness-AI.

---

## 8. AI-Literacy

Erfüllung der Pflicht aus AI Act Art. 4 (gilt seit 02.02.2025):

- **Onboarding für neue Crew-Mitglieder:** Diese Richtlinie wird mit Eintritt durchgegangen, Kenntnisnahme dokumentiert
- **Quartalsweises Update:** Bei Quartals-Review des Inventars werden auch Änderungen der Richtlinie kommuniziert
- **Schulungs-Log:** kurze Notiz im Studio-Wiki / Notion / o.ä. mit Datum + Teilnehmer:innen

---

## 9. Bei Verstößen

Wenn etwas schief geht (KI-Output ohne Review rausging, Tool ohne DPA genutzt wurde, Kennzeichnung vergessen):

1. Sofort melden an Studio-Leitung
2. Schaden eindämmen (Veröffentlichung stoppen, Korrektur publizieren, Kunde informieren)
3. Ursachenanalyse + Anpassung dieser Richtlinie, falls notwendig

Kein Vorwurf-Fokus. Lernen-Fokus.

---

## 10. Review-Zyklus

Diese Richtlinie wird **mindestens einmal pro Jahr** überprüft, oder anlassbezogen wenn:
- Neue Tools ins Inventar kommen, die neue Risiken einführen
- AI-Act-Vorgaben sich ändern (z.B. neue Stichtage)
- Vorfall (siehe §9) Handlungsbedarf zeigt

**Letztes Review:** 2026-05-04
**Nächstes Pflicht-Review:** 2027-05-04
