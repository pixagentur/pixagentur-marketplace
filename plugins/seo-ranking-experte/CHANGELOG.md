# Changelog

Alle nennenswerten Änderungen an diesem Skill werden hier dokumentiert. Format orientiert sich an
[Keep a Changelog](https://keepachangelog.com/), Versionierung folgt
[Semantic Versioning](https://semver.org/) (`MAJOR.MINOR.PATCH`).

Die genauen Regeln, wann welche Stelle der Versionsnummer erhöht wird, stehen in
`references/20-pflege-und-versionierung.md` (Abschnitt "Skill-Versionierung").

## [1.4.0] – 2026-09-17

### Hinzugefügt
- **Zweiter Modus „Neuerstellung".** Der Workflow kannte bisher nur das Prüfen einer
  bestehenden URL. Das Regelwerk trägt beide Fälle, also musste man den Workflow umgehen,
  um beim Schreiben an die Regeln zu kommen. Schritt 0 fragt den Modus jetzt ab; im Modus
  Neuerstellung entfallen Schritt 1, 3 und 6, Schritt 5 wird von der Swap-Liste zur
  Schreibvorgabe, und Schritt 7 wird durch eine Selbstprüfung gegen
  `references/03-audit-checkliste.md` ersetzt, mit ausdrücklicher Kennzeichnung der
  Kategorien, die erst nach dem Livegang messbar sind.
- **R-HEAD-025** in `references/14-regeln-ueberschriften.md`: Die Überschrift greift die
  Formulierung der Suchanfrage auf, nicht nur deren Thema, Symptom- und
  Problemformulierungen eingeschlossen. Gegenstück zu R-HEAD-001: Ohne eine Gebotsregel
  neben der Verbotsregel wird aus „Keywords sind kein Rankingfaktor" in der Anwendung „die
  Suchsprache ist egal", und es entstehen Überschriften, die niemand sucht. Begründet wird
  sie nicht mit Ranking, sondern mit Wiedererkennung, Passage Ranking und Snippet-Qualität.

## [1.3.0] – 2026-07-16

### Hinzugefügt
- Neues Regelwerk `references/14-regeln-ueberschriften.md` (R-HEAD-001 bis R-HEAD-024):
  trennt, was Überschriften nachweislich bewirken (Ergebniszeile im SERP, Passage Ranking,
  Zitierfähigkeit, Überfliegbarkeit), von der verbreiteten Fehlannahme, Suchbegriffe in
  Überschriften seien ein eigener Rankingfaktor.
- Vier neue Prüfpunkte in `03-audit-checkliste.md` Kategorie B, mit Verweis auf die
  entsprechenden R-HEAD-Regeln.

### Geändert
- `03-audit-checkliste.md`: Prüfpunkt "H1 einmalig vorhanden" entfernt (R-HEAD-003 – mehrere
  H1 sind kein Fehler) und durch die vier neuen, differenzierteren Punkte ersetzt.
- `R-CONTENT-020` (`11-regeln-content-eeat.md`) auf Title-Tag/Meta-Description reduziert;
  Überschriften-Teil ausgelagert nach `14-regeln-ueberschriften.md`, um zwei widersprüchliche
  Aussagen zum selben Thema zu vermeiden.
- `SKILL.md`: Regelwerk-Referenzen von `references/10`–`13` auf `10`–`14` erweitert (3 Stellen),
  neue Datei in der Referenz-Tabelle ergänzt.
- `references/20-pflege-und-versionierung.md`: Kategorie `HEAD` im ID-Schema ergänzt.

## [1.2.0] – 2026-07-15

### Hinzugefügt
- Neuer PDF-Abschnitt "Was bereits gut läuft": listet bereits erfüllte/positive Befunde aus der
  Audit-Checkliste, gruppiert nach Kategorie (`build_report`, neues optionales Datenfeld
  `"staerken"`, Funktion `_positive_findings_block` in `scripts/generate_report_pdf.py`).
- Schritt 2 in `SKILL.md` erweitert: neben Mängeln jetzt auch konkret erfüllte Checklisten-
  Punkte notieren, als Grundlage für den neuen PDF-Abschnitt.

## [1.1.0] – 2026-07-14

### Hinzugefügt
- Feste Standardregel für Website-weite Analysen (mehrere URLs): immer ein vollständiger
  PDF-Report pro URL plus ein zusätzliches, übergreifendes Executive-Summary-PDF – keine
  Rückfrage beim Intake mehr nötig (`SKILL.md` Schritt 7).
- `build_summary_report()` in `scripts/generate_report_pdf.py`: neues, eigenständiges PDF mit
  Score-Vergleich (Balkendiagramm), Seiten-Übersichtstabelle und optionalen
  seitenübergreifenden Erkenntnissen.

### Geändert
- Referenz auf den `pdf`-Skill in Schritt 7 präzisiert (nur noch für optionale
  Nachbearbeitung, nicht mehr für das Zusammenführen mehrerer Reports – das übernimmt jetzt
  `build_summary_report`).

## [1.0.0] – 2026-07-14

Erste vollständige Fassung mit allen Kernfunktionen. Erstveröffentlichungsstand für GitHub
Marketplace.

### Hinzugefügt
- Bewertungssystem: Gesamt-Score von 0–1.000 Punkten mit Kategorien-Gewichtung und
  Deckelungsregeln für K.O.-Mängel (`references/05-bewertungssystem.md`).
- Automatische PDF-Report-Erzeugung am Ende jeder Analyse, inkl. Score-Gauge-Chart und
  Kategorie-Balkendiagramm (`scripts/generate_report_pdf.py`).
- Klare Unterscheidung in der Text-Swap-Liste zwischen "Text ersetzen" (Ist-Text/Neu-Text) und
  "neuen Text einfügen" (mit Stellenangabe).
- Skill-Versionierung inkl. dieser Changelog-Datei.

### Geändert
- Regelwerk vollständig auf Basis aller 13 vom Auftraggeber vorgegebenen Fachquellen plus
  offizieller Google-Dokumentation synthetisiert und in vier Themendateien strukturiert
  (`references/10`–`13`), mit eindeutigen Regel-IDs statt Fließtext.
- Keine Quellen-/Autor:innen-Nennung mehr im Skill-Output – das Regelwerk wird als eigenständiges
  angewandtes Fachwissen dargestellt (siehe `references/20-pflege-und-versionierung.md`).

### Entfernt
- Frühere Dateien `01-google-regeln.md`, `02-blog-insights.md`, `05-quellenverzeichnis.md`
  (ersetzt durch das konsolidierte, quellenfreie Regelwerk `10`–`13`).

## [0.2.0] – 2026-07-14 (nicht veröffentlicht, interner Zwischenstand)

### Hinzugefügt
- Intake-Fragen (`00-intake-fragen.md`) und Audit-Checkliste mit Ampel-Logik
  (`03-audit-checkliste.md`).
- Schreibstil- und Natürlichkeits-Leitfaden (`04-schreibstil-und-natuerlichkeit.md`).
- Erster Regel-Entwurf auf Basis offizieller Google-Quellen, plus grobe Einordnung der
  vorgegebenen Fachblog-Liste (mit Quellenangaben – später in 1.0.0 entfernt).

## [0.1.0] – 2026-07-14 (nicht veröffentlicht, erster Entwurf)

### Hinzugefügt
- Grundgerüst des Skills: SKILL.md mit Workflow-Skizze, README, LICENSE (MIT).
- Erste, noch unvollständige Quellenrecherche zu offiziellen Google-Ranking-Kriterien.

---

## Format für zukünftige Einträge

```
## [MAJOR.MINOR.PATCH] – JJJJ-MM-TT

### Hinzugefügt
- ...

### Geändert
- ...

### Behoben
- ...

### Entfernt
- ...
```

Nur die tatsächlich zutreffenden Unterabschnitte verwenden, leere Abschnitte weglassen.
