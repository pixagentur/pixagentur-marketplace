# Changelog

Alle nennenswerten Änderungen an diesem Skill werden hier dokumentiert. Format orientiert sich an
[Keep a Changelog](https://keepachangelog.com/), Versionierung folgt
[Semantic Versioning](https://semver.org/) (`MAJOR.MINOR.PATCH`).

Die genauen Regeln, wann welche Stelle der Versionsnummer erhöht wird, stehen in
`references/20-pflege-und-versionierung.md` (Abschnitt "Skill-Versionierung").

## [1.5.0] – 2026-10-08

### Hinzugefügt
- **Dritter Modus „Überarbeitung einer Live-Seite".** Der häufigste Fall, eine bestehende
  Seite verbessern und die Änderungen gleich einspielen, passte weder in Audit (Ergebnis ist
  ein Report) noch in Neuerstellung (keine Seite zum Messen). Schritt 1 und 2 laufen wie im
  Audit, Schritt 5 wird zur direkten Umsetzung mit Vorher/Nachher-Protokoll im Chat, Score
  und PDF entstehen nur auf Wunsch.
- **Ableiten statt fragen, mit Grenze** (Schritt 0, `references/00-intake-fragen.md`):
  Intake-Punkte dürfen aus dem Bestand beantwortet werden, wenn die Seite eine bestehende
  Leistung behandelt, und werden im Abschluss als Annahmen genannt. Bei neuer Leistung,
  neuem Produkt oder neuem Markt wird mindestens die Zielgruppe ausdrücklich gefragt.
  Intake-Frage zum Modus um die dritte Option ergänzt.
- **R-TECH-006** in `references/10-regeln-technik-performance.md` (K.O.): Antwortkopf
  (Status, `x-robots-tag`, `retry-after`, `meta robots`) getrennt vom Inhalt prüfen, je
  Seitentyp. Eine Seite kann vollständigen Inhalt mit `503` und `noindex` ausliefern. Dazu
  ein Unterpunkt in Schritt 1 und der präzisierte Prüfpunkt in
  `references/03-audit-checkliste.md` Kategorie A.
- **Reihen-Prüfung im Modus Neuerstellung:** Bei einem weiteren Beitrag einer Reihe
  zuerst die Gliederung der letzten Beiträge lesen und Reihenfolge, Kapitelform und
  Abschluss bewusst variieren. Die Pflichtbestandteile bleiben.
- Abschnitt **„Was die Stilregeln leisten und was nicht"** in
  `references/04-schreibstil-und-natuerlichkeit.md`, mit Kalibrierverfahren für den Fall,
  dass eine Prüfung auf maschinelle Herkunft verlangt wird (mindestens zwei Detektoren
  unterschiedlicher Stärke plus Gegenprobe an einem gesichert von Hand geschriebenen Text).

### Geändert
- **Beschreibung (Frontmatter):** Das Versprechen „Text-Ersetzungsvorschläge …, die nicht
  als KI-generiert erkennbar sind" entfernt. Die Stilregeln sind nicht gegen einen
  Detektor kalibriert; an einem Text, der jede Regel einhielt, urteilte der stärkste
  Detektor 100 % maschinell. Die Beschreibung nennt jetzt die drei Modi und bindet den
  automatischen PDF-Report an den Modus Audit.
- Schritt 7: PDF-Pflicht gilt ausdrücklich für den Modus Audit (in 1.4.0 widersprach die
  Überschrift „immer am Ende" dem Modus Neuerstellung).
- Schritt 5 und „Grenzen dieses Skills": Stilregeln richten sich an Leser:innen, kein
  Nachweis gegenüber KI-Detektoren.
- `README.md`: Versionsangabe nachgezogen (stand seit 1.3.0 auf 1.3.0).

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
