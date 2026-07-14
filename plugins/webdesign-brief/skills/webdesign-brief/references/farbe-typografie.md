# Farbe & Typografie

## Farbe: Systematik statt konkreter Werte

Diese Regeln legen keine konkreten Farbwerte (kein Hex/RGB) fest — die Palette ist immer projekt-/kundenspezifisch. Unabhängig von der gewählten Palette gilt aber:

- **Maximal 2–3 Farbrollen pro Projekt**, jede mit klarer Aufgabe.
- **60-30-10-Regel**:
  - 60 % Neutraltöne für Hintergrund und Fließtext.
  - 30 % Sekundärfarbe für Flächen, Karten, Header-Bereiche.
  - 10 % Akzentfarbe für CTAs, Buttons, alles, was Aufmerksamkeit verdient.
- Statt zusätzliche Farben einzuführen: die Primärfarbe über Opacity-/Helligkeitsstufen variieren, um Varianten zu erzeugen, ohne die Palette zu vergrößern.
- Liegt eine Kunden-CI/Markenfarbe vor: diese als Ausgangspunkt nehmen und Rollen (Primär/Sekundär/Akzent) daraus ableiten, statt eine neue Palette zu erfinden.
- Sind keine Farben vorgegeben: beim Nutzer nachfragen (Schritt 0, Punkt C) oder — falls delegiert — eine dezente, zur Zielgruppe passende Palette anhand der obigen Rollen-Logik recherchieren/vorschlagen, ohne selbst Hex-Werte zu fixieren, sofern nicht ausdrücklich verlangt.

## Typografie

### Schriftwahl — lizenzfrei und kommerziell nutzbar

- Schriften müssen uneingeschränkt kommerziell nutzbar sein. **Google Fonts bevorzugen** (durchgehend Open-Font-Lizenzen, kostenlos, kommerziell nutzbar, einfach einzubinden).
- Wird eine Schrift aus anderer Quelle vorgeschlagen: explizit prüfen und benennen, dass eine kommerzielle Nutzungslizenz vorliegt (z. B. SIL Open Font License). Im Zweifel bei Google Fonts bleiben.
- **Maximal 2 Schriftfamilien** pro Projekt (eine für Headlines, optional eine zweite für Fließtext) — außer ein bestehendes Corporate Design gibt etwas anderes vor.
- Schriftwahl an Zielgruppe/Branche anpassen (seriös/klassisch vs. modern/verspielt vs. technisch/klar).

### Type-Scale-System (statt Schriftgrößen zu erraten)

- Basisgröße Fließtext: **16px**.
- Skalierungsfaktor: ca. **1,25 (Major Third)** zwischen den Ebenen — Größe wächst konsistent um ~25 % pro Stufe von H6 bis H1.
- Globale Schriftgrößen als Kaskade anlegen (**rem-Werte, nicht px**), damit die Skala überall konsistent bleibt und Änderungen an der Basisgröße alles proportional mitskalieren.
- **Letter-Spacing**: Fließtext unverändert lassen (Standard = beste Lesbarkeit). Überschriften, besonders große, leicht negativ (enger) einstellen.
- **Line-Height**: Fließtext ≈ 150 % der Schriftgröße (16px → 24px). Überschriften enger (110–130 %), damit sie kompakter und wirkungsvoller wirken.
