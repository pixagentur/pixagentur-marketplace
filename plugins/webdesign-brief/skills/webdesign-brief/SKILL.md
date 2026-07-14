---
name: webdesign-brief
description: 'Verpflichtendes Intake-Briefing für JEDEN neuen Webdesign-Auftrag — anwenden, sobald jemand eine neue Webseite erstellen will, eine neue Landingpage bauen will, oder eine bestehende Webseite neu gestalten/redesignen will. Fragt vor jeglichem Design- oder Code-Output zuerst Branche, Kunde, Farben, Hero-Layout, Animationen, Hintergrund, Bildmaterial, Referenzen, Tech-Stack, Umfang, Conversion-Ziel und Sprache aktiv über Rückfragen ab, und setzt danach verbindliche Regeln für Farbsystem, Typografie, Grid/Spacing, Barrierefreiheit (WCAG AA), Conversion-Komponenten und SEO durch. Muss VOR dem frontend-design-Skill laufen. Trigger-Beispiele: neue Webseite erstellen, Landingpage bauen, Webseite neu gestalten/redesignen, Website für Branche/Kunde.'
---

# Webdesign-Brief

Dieser Skill ist das verpflichtende Tor vor jedem Webdesign-Task. Er wird IMMER zuerst ausgeführt, bevor eine Zeile Design oder Code entsteht — auch wenn der Nutzer selbst nicht danach fragt.

**Nicht überspringen, nicht raten.** Auch wenn eine Antwort aus dem Kontext ableitbar erscheint (z. B. Branche impliziert vermeintlich eine Farbwahl), wird trotzdem aktiv gefragt. Der Nutzer will bewusst ausführlich befragt werden, um eine besonders kreative, auf ihn zugeschnittene Seite zu bekommen — ein übersprungener Punkt ist ein Fehler, kein Zeitgewinn.

## Wann dieser Skill greift

Sofort anwenden, wenn der Nutzer sinngemäß sagt:
- "Ich möchte eine neue Webseite erstellen"
- "Ich möchte eine neue Landingpage bauen"
- "Ich möchte eine bestehende Webseite neu gestalten / redesignen"
- Jede Variante davon (auch ohne exakten Wortlaut) — z. B. "Baue mir eine Seite für...", "Wir brauchen einen Website-Relaunch"

Nicht nötig bei: reinen Bugfixes, kleinen Textänderungen, isolierten Komponenten-Anpassungen an einer bereits gebrieften Seite innerhalb desselben Projekts (dann reicht der `frontend-design`-Skill bzw. direkte Umsetzung).

## Wie gefragt wird

Für alle Fragen mit klaren Auswahloptionen das strukturierte Rückfrage-Tool der jeweiligen Umgebung verwenden (in Claude Code: `AskUserQuestion`; in anderen Umgebungen das dortige Äquivalent), so oft hintereinander wie nötig, bis wirklich jede unten gelistete Frage mit allen genannten Optionen gestellt wurde. Der volle Umfang aus A–L wird immer komplett gestellt — nichts wird zusammengefasst, gekürzt oder ausgelassen. Steht in der aktuellen Umgebung kein strukturiertes Rückfrage-Tool zur Verfügung, dieselben Fragen mit denselben Optionen stattdessen als nummerierte Liste im Chat stellen.

Für offene Angaben ohne sinnvolle Auswahlliste (Kundenname, Branche im Detail, eigene Markenfarben, Screenshots/Links) stattdessen normale Rückfrage im Chat stellen.

## Schritt 0: Verpflichtendes Intake — IMMER zuerst, keine Ausnahme

Bevor irgendein Vorschlag, Mockup oder Code entsteht, folgende Punkte klären. Antworten, die der Nutzer schon im ursprünglichen Prompt mitgeliefert hat, nicht erneut abfragen — nur die Lücken. Aber: "könnte man ableiten" zählt nicht als beantwortet.

**A) Branche** — Welche Branche/welches Segment? (bestimmt Stiltyp: seriös/klassisch, modern/verspielt, technisch/klar, luxuriös, etc.)

**B) Kunde** — Name des Kunden und was er konkret macht (Produkt/Dienstleistung, Zielgruppe, Alleinstellung). Gibt es keinen konkreten Kunden, ist die Branche allein ausschlaggebend — das explizit festhalten.

**C) Farben** — Gibt es ein bestehendes Design-System / CI-Farben? Falls ja: verwenden, Rollen daraus ableiten. Falls nein: selbst recherchieren (aktuelle Trends einbeziehen) und Vorschlag machen. Details zur Farb-Systematik: [references/farbe-typografie.md](references/farbe-typografie.md).

**D) Hero-Bereich** — strukturiert abfragen:

*Runde D1:*
1. "Breite des Hero-Bereichs?" — Optionen: Volle Breite / Nur Content-Breite
2. "Spalten im Hero-Bereich?" — Optionen: Einspaltig / Mehrspaltig
3. "Horizontale Ausrichtung im Hero?" — Optionen: Links / Zentriert / Rechts

*Runde D2:*
1. "Vertikale Ausrichtung im Hero?" — Optionen: Oben / Mittig / Unten
2. "Hintergrund des Hero-Bereichs?" — Optionen: Bild / Video / Animation / Kombination mit Overlay

Inspiration: [21st.dev Hero-Komponenten](https://21st.dev/community/components/s/hero)

**E) Animationen & Scroll-Effekte** — strukturiert abfragen:

1. Einzelfrage (single-select): "Wie viel Animation soll die Seite haben?"
   - "Durchgehend, viele Bereiche"
   - "Dezent, nur ausgewählte Bereiche"
   - "Keine Animationen"

   Bei "Keine Animationen": Punkt E beendet, weiter zu F. Sonst weiter mit 2 und 3.

2. Multiselect-Frage: "In welchen Bereichen? (Teil 1)"
   - Hero-Bereich (Eingangsanimation)
   - Section-Reveals beim Scrollen (Einblenden von Inhalten)
   - Hover-/Micro-Interactions (Buttons, Cards, Links)
   - Zähler-/Statistik-Animationen (Zahlen hochzählen)

3. Multiselect-Frage: "In welchen Bereichen? (Teil 2)"
   - Parallax-Effekte (Hintergrund/Bild bewegt sich versetzt zum Scroll)
   - Sticky-Elemente (Navigation/Sidebar bleibt beim Scrollen stehen)
   - Hintergrund-Shader/Canvas-Animation (generative/ambiente Bewegung im Hintergrund)
   - Keine weiteren

Inspirationsquelle für Shader/Animationen: [21st.dev Shader-Komponenten](https://21st.dev/community/components/s/shader) — gezielt danach suchen, ob eine der dortigen Vorlagen (Shader, generative Hintergründe, Hero-Animationen) für Hero (D) oder globalen Hintergrund (F) passt, und dem Nutzer konkret vorschlagen statt nur allgemein zu verweisen. Umsetzung siehe `gsap-skills:*`-Skills (ScrollTrigger, Timeline, Performance) sobald Konzept steht.

**F) Website-Hintergrund (global)** — strukturiert abfragen:
1. "Hintergrundstil der gesamten Website?" — Optionen: Einfarbig / Wechselt je Section / Mehrfarbig mit Verlauf
2. "Soll im Hintergrund durchgehend eine Animation laufen (z. B. Shader/generativ)?" — Optionen: Ja / Nein

Bei "Ja": auf dieselbe 21st.dev-Shader-Quelle wie in E zurückgreifen und konkrete Vorschläge machen.

**G) Zielplattform / Tech-Stack** — WordPress/Elementor, Webflow, reiner Code (z. B. React/Next.js), Shopify, o. ä. Bestimmt, wie Grid/Spacing/Code technisch umgesetzt werden (Elementor-Container vs. CSS-Grid/Flexbox, Component-Library wie `shadcn` bei React-Stack).

**H) Umfang & Sitemap** — Einzelne Landingpage oder Multi-Page-Website? Grobe Seitenanzahl/-struktur.

**I) Conversion-Ziel** — Was soll der Besucher tun? Lead-Formular, Terminbuchung, Kauf, reine Information. Bestimmt CTA-Typ und Formularlänge.

**J) Sprache(n) & Zielmarkt** — In welcher(n) Sprache(n) geht die Seite live, welcher Zielmarkt/welche Region.

**K) Bildmaterial** — strukturiert abfragen: "Wie soll das Bildmaterial (Fotos, Logos, Grafiken) entstehen?"
- Eigene Bilder/Logos vorhanden (Nutzer liefert)
- Alles per Higgsfield generieren
- Mix: eigenes Material + Ergänzung per Higgsfield

Bei "Eigene Bilder/Logos vorhanden": im Chat nachfragen, welche Dateien/Links das sind. Details zur Higgsfield-Nutzung: Schritt 2.

**L) Referenzen & Vorlagen** — strukturiert abfragen: "Hast du schon konkrete Referenzseiten, Screenshots oder Vorlagen im Kopf?"
- Ja, ich schicke Referenzen/Screenshots/Links
- Nein, bitte selbst recherchieren

Bei "Ja": im Chat auf die konkreten Links/Screenshots warten, bevor mit Schritt 1 begonnen wird. Bei "Nein": direkt mit Schritt 1 fortfahren.

Erst wenn A–L beantwortet sind, weiter zu Schritt 1. Wird eine einzelne Frage vom Nutzer nicht beantwortet oder ohne Auswahl übersprungen, **nicht erneut nachfragen und den Prozess nicht stoppen** — stattdessen selbst eine sinnvolle Standardoption wählen (passend zu Branche/Stil aus den übrigen Antworten) und diese Annahme in der Zusammenfassung am Ende (Schritt 4) kurz benennen.

## Schritt 1: Inspiration recherchieren

Bevor eigene Vorschläge gemacht werden, passende Referenzen suchen (sofern der Nutzer bei L nicht schon eigene Referenzen geliefert hat):
- [bestwebsite.gallery](https://bestwebsite.gallery/) — mit Keywords aus Branche/Stil durchsuchen, oder Nutzer nach Screenshots fragen
- [dribbble.com](https://dribbble.com/) — Alternative/Ergänzung, gleiches Vorgehen
- [21st.dev](https://21st.dev/community/components/s/hero) — für Hero- und Shader-Komponenten (siehe D/E/F)

Wenn eine Quelle Login erfordert (z. B. um Code von 21st.dev zu exportieren): Nutzer nach Zugangsdaten fragen, ODER anbieten, dass der Nutzer selbst kurz etwas Passendes raussucht und die Fundstelle/den Code mitteilt.

Mehr dazu: [references/quellen-tools.md](references/quellen-tools.md).

## Schritt 2: Medien (Bild/Video/Audio) über den Higgsfield-Skill

Für alle Bilder, Videos und sonstigen Medien-Assets, die laut K per Higgsfield entstehen sollen, den `higgsfield-media-generation`-Skill konsultieren, bevor irgendein Higgsfield-MCP-Tool (`mcp__cb36b77b-79c9-4852-8786-51f529b8ab22__*`, z. B. `generate_image`, `generate_video`) direkt aufgerufen wird — der Skill legt Modell-Defaults, Auflösungs-Regeln und einen verpflichtenden Bestätigungs-Workflow fest. Details: [references/quellen-tools.md](references/quellen-tools.md).

## Schritt 3: Design-Regeln anwenden

Sobald Intake + Inspiration stehen, gelten verbindlich:
- **Farbe & Typografie** — [references/farbe-typografie.md](references/farbe-typografie.md)
- **Layout, Grid, Spacing, Barrierefreiheit** — [references/layout-a11y.md](references/layout-a11y.md)
- **Conversion-Komponenten & SEO** — [references/conversion-seo.md](references/conversion-seo.md)
- **Code-Qualität**: semantische HTML-Struktur, CSS-Klassen statt Inline-Styles, JS/Animationsbibliotheken nur wenn reines CSS nicht reicht, zusätzliche Logik (PHP/JS) minimal-invasiv und kommentiert.

## Schritt 4: Umsetzung — an spezialisierte Skills übergeben

Dieser Skill liefert das Briefing und die harten Regeln, nicht die kreative Ausführung. Für die eigentliche Umsetzung:
- **Ästhetik/Visuelles Design & Code** → `frontend-design`-Skill (bestehend, nicht duplizieren)
- **Scroll-Animationen, Timelines, Performance** → `gsap-skills:*` (gsap-core, gsap-scrolltrigger, gsap-timeline, gsap-react, gsap-frameworks, gsap-performance, gsap-plugins, gsap-utils)
- **React-Komponenten/Component-Library** (falls Tech-Stack = React) → `shadcn`-Skill
- **SEO-Umsetzung** → `searchfit-seo:*` (seo-audit, on-page-seo, content-brief, schema-markup, keyword-clustering, technical-seo, internal-linking)
- **Barrierefreiheits-Review** → `design:accessibility-review`
- **Medien** → `higgsfield-media-generation`-Skill (Schritt 2)

Am Ende kurz zusammenfassen, welche Antworten aus Schritt 0 die getroffenen Design-Entscheidungen begründen — nicht nur das Ergebnis zeigen, sondern die Ableitung aus dem Briefing sichtbar machen. Alle Punkte, bei denen Claude mangels Antwort selbst entschieden hat, hier explizit als solche kennzeichnen.
