# Layout, Responsiveness & Barrierefreiheit

## Grid

- Desktop: 12 Spalten. Tablet: 8 Spalten. Mobile: 4 Spalten.
- Im jeweiligen Tool nachbilden (Elementor-Container/Flexbox mit definierten Spaltenanteilen wie 6/6, 4/4/4, 8/4; bei Code entsprechend CSS-Grid/Flexbox).

## Spacing (8-Punkt-Grid)

- Alle Abstände (Padding, Margin, Gaps) sind Vielfache von 8: 8, 16, 24, 32, 40, 48, 64, 80, 96, 128 px.
- Keine "krummen" Werte wie 15px oder 22px — das sorgt für den unbewussten "aufgeräumten" Eindruck professioneller Sites.
- Als globale Spacing-Presets bzw. CSS-Variablen anlegen, damit jede Section/jedes Widget darauf zurückgreift statt Werte einzeln neu einzutippen.

## Visuelle Hierarchie — vier Werkzeuge, zusammen eingesetzt

- **Nähe (Proximity)**: Zusammengehörige Elemente eng gruppieren, unabhängige Blöcke klar trennen.
- **Größe**: Wichtigeres größer, Unwichtigeres kleiner.
- **Kontrast**: über Größe, Schriftschnitt oder Deckkraft/Farbrolle (nicht konkrete Farbwerte) signalisieren, was zuerst gelesen werden soll.
- **Ausrichtung**: konsequente Kantenausrichtung entlang des Grids — keine "fast" ausgerichteten Elemente.

Nutzer scannen Seiten, sie lesen sie nicht linear. Das Layout muss das Auge aktiv führen.

## Responsive Pflicht

- Jede Seite muss auf allen gängigen Geräteklassen einwandfrei funktionieren: Desktop, Tablet, Mobile (Portrait & Landscape).
- Breakpoints konsequent testen/mitdenken (typisch: ≥1200px Desktop, 768–1199px Tablet, <768px Mobile — im jeweiligen Tool/Framework anpassen).
- Touch-Ziele auf Mobile ausreichend groß (mind. ca. 44×44px), Navigation auf kleinen Screens auf ein Mobile-Menü umstellen, Bilder/Hintergründe skalieren statt abgeschnitten zu werden.

## Barrierefreiheit: WCAG mindestens AA

Verbindlicher Standard, keine Ausnahme:

- **Kontrast**: mind. 4,5:1 für normalen Text, 3:1 für großen/fetten Text und für UI-Komponenten/Grafiken.
- **Semantische Struktur**: korrekte HTML-Elemente (`nav`, `header`, `main`, `footer`, `button` vs. `div`), keine reinen Div-Suppen.
- **Tastaturbedienbarkeit**: alle interaktiven Elemente (Menüs, Formulare, Buttons, Slider) müssen ohne Maus bedienbar sein, inkl. sichtbarem Fokus-Stil.
- **Alt-Texte** für alle bedeutungstragenden Bilder; dekorative Bilder als solche markieren.
- **Formulare**: Labels korrekt mit Feldern verknüpft, Fehlermeldungen klar und nicht nur farblich codiert.
- **Bewegte Elemente/Animationen**: sparsam einsetzen, keine schnell blinkenden Effekte; wo sinnvoll `prefers-reduced-motion` respektieren.
- Bei jedem Design/Review aktiv gegenprüfen, nicht nur "sieht barrierefrei genug aus" annehmen. Bei Bedarf `design:accessibility-review`-Skill hinzuziehen.
