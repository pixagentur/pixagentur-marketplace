# Inspirationsquellen & Tools

## Design-Inspiration

- **[bestwebsite.gallery](https://bestwebsite.gallery/)** — mit Keywords aus Branche/Stil (z. B. "SaaS dark minimal", "restaurant warm editorial") durchsuchen. Wenn kein direkter Zugriff/Suchergebnis möglich: Nutzer nach Screenshots passender Referenzen fragen.
- **[dribbble.com](https://dribbble.com/)** — Alternative bzw. Ergänzung zu bestwebsite.gallery, gleiches Vorgehen (Keyword-Suche oder Screenshots erfragen).
- **[21st.dev – Hero-Komponenten](https://21st.dev/community/components/s/hero)** — Inspiration für Schritt 0, Punkt D (Hero-Layout).
- **[21st.dev – Shader-Komponenten](https://21st.dev/community/components/s/shader)** — Inspiration für Schritt 0, Punkt E/F (Animationen/Hintergrund-Effekte). Wird für die Umsetzung ein Login/Export nötig: Nutzer nach Zugangsdaten fragen, oder anbieten, dass der Nutzer selbst kurz etwas Passendes raussucht und Fundstelle/Code mitteilt.

Gefundene Referenzen immer kurz einordnen (was genau daran passt: Layout? Farbstimmung? Bewegung?) statt nur den Link/Screenshot zu übernehmen.

## Medien-Erstellung: Higgsfield-Skill

Für Bilder, Videos, Audio und weitere Medien-Assets (Schritt 0, Punkt K) den `higgsfield-media-generation`-Skill nutzen, statt Higgsfield-MCP-Tools (`mcp__cb36b77b-79c9-4852-8786-51f529b8ab22__*`) direkt aufzurufen — der Skill legt Modell-Defaults (Nano Banana Pro, GPT Image 2, Seedance 2.0), Auflösungs-Regeln (2K für Bilder, 4K für Video), Aspect-Ratio-Defaults nach Plattform und einen verpflichtenden Bestätigungs-Workflow fest, bevor überhaupt generiert wird.

Ist der Higgsfield-Skill in der aktuellen Umgebung nicht verfügbar, ersatzweise direkt die MCP-Tools nutzen: `generate_image`, `generate_video`, `generate_audio` (Kernerstellung), vorab `models_explore` (`action: 'recommend'`) bei Unsicherheit über das passende Modell, sowie `upscale_image`/`upscale_video`, `outpaint_image`, `reframe`, `remove_background`, `motion_control` für gezielte Nachbearbeitung. Lokale Nutzer-Dateien (Fotos/Logos) über `media_upload_widget` einbinden, nicht per Chat-Attachment erwarten.

## Verwandte Skills (bei Bedarf referenzieren/aufrufen)

- **`frontend-design`** — kreative Ästhetik-Umsetzung (Farbe, Typografie im Detail, Motion, Spatial Composition). Wird nach Abschluss von Schritt 0–3 dieses Skills aufgerufen, nicht dupliziert.
- **`gsap-skills:gsap-core`**, `gsap-scrolltrigger`, `gsap-timeline`, `gsap-react`, `gsap-frameworks`, `gsap-performance`, `gsap-plugins`, `gsap-utils` — für die technische Umsetzung von Scroll-Effekten/Animationen aus Schritt 0, Punkt E.
- **`shadcn`** — Component-Library, wenn Tech-Stack (Schritt 0, Punkt G) React ist.
- **`higgsfield-media-generation`** — für alle Medien aus Schritt 0, Punkt K.
- **`searchfit-seo:*`** — siehe [conversion-seo.md](conversion-seo.md).
- **`design:accessibility-review`** — vertiefte Barrierefreiheits-Prüfung.
