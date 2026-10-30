# Intake-Fragen

Diese Fragen werden **vor** jeder Analyse gestellt. Ziel: genug Kontext, um Empfehlungen und
Textvorschläge treffsicher statt generisch zu machen. Bereits im Prompt beantwortete Punkte
nicht erneut abfragen.

Bevorzugt über `ask_user_input_v0` stellen (Buttons statt Freitext, wo sinnvoll). Beispiel-Setup:

```json
{
  "questions": [
    {
      "question": "Was soll am Ende herauskommen?",
      "options": ["Audit mit Report (bestehende Seite)", "Neuer Text (Seite noch nicht live)", "Bestehende Seite direkt überarbeiten"]
    },
    {
      "question": "Analysieren wir eine einzelne URL oder die ganze Website?",
      "options": ["Einzelne URL", "Ganze Website/Domain", "Mehrere bestimmte URLs"]
    },
    {
      "question": "Was ist das Hauptziel dieser Seite(n)?",
      "options": ["Leads/Kontaktanfragen", "Direktverkauf", "Markenbekanntheit/Reichweite", "Informations-/Ratgeberzweck"]
    },
    {
      "question": "Soll der bestehende Schreibstil beibehalten werden?",
      "options": ["Ja, 1:1 Stil beibehalten", "Stil leicht anpassen erlaubt", "Ich habe ein Styleguide/Beispiel"]
    }
  ]
}
```

Danach als Freitext-Rückfragen ergänzen (bei Bedarf, max. so viele wie nötig):

- Zielgruppe genauer: Branche, B2B/B2C, Fachwissen-Level, Region/Sprache?
- Was weiß diese Zielgruppe über den Gegenstand schon? (Entscheidet in Schritt 2a, ob ein
  erklärender Abschnitt Zielinhalt ist oder am Kundenkreis vorbeigeht.)
- Gibt es Ziel-Keywords oder Themen, für die die Seite gefunden werden soll?
- Gibt es bekannte Mitbewerber-URLs, die aktuell besser ranken?
- Betrifft der Inhalt YMYL-Themen (Gesundheit, Recht, Finanzen, Sicherheit)? Falls ja: gibt es
  Autor:innen mit nachweisbarer Fachexpertise, die genannt werden können?
- Gibt es Zugriff auf Google Search Console / Analytics-Daten, die die Analyse unterstützen
  könnten (bei angebundenen Connectors direkt nutzen)?
- Gibt es ein Corporate-Design/Textstyleguide, das beachtet werden muss?

## Wann aus dem Bestand abgeleitet werden darf

Im Modus Überarbeitung (und bei Neuerstellungen für eine bestehende Leistung) dürfen Ziel,
Stil, Region und Zielgruppe aus der Seite und ihren Schwesterseiten abgeleitet statt
gefragt werden; jede Ableitung wird im Abschluss als Annahme genannt. **Nicht** abgeleitet
wird bei einer neuen Leistung, einem neuen Produkt oder einem neuen Markt: Dann mindestens
die Zielgruppe (B2B/B2C, Branche) ausdrücklich fragen, bevor Beispiele, Bilder oder Texte
entstehen. Der Bestand sagt über etwas Neues nichts aus, er liefert nur eine plausible
Vorlage, und die verdeckt, dass die Frage offen ist.

## Warum diese Fragen wichtig sind

- **Ziel & Zielgruppe** bestimmen, welche Keywords/Suchintentionen überhaupt relevant sind –
  ohne das ist jede Keyword-Empfehlung geraten. Der Wissensstand der Zielgruppe gehört dazu:
  Eine Platzierung belegt Passung zur Suchanfrage, nicht zum eigenen Kundenkreis.
- **Schreibstil-Vorgabe** ist Voraussetzung dafür, dass die Text-Swap-Liste in Schritt 5 nicht
  wie ein Fremdkörper auf der Seite wirkt.
- **YMYL-Status** entscheidet, wie strikt E-E-A-T-Signale (Autor:innen-Nachweis, Quellenangaben,
  Aktualität) eingefordert werden müssen.
