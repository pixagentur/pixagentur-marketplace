# Audit-Checkliste (Ampel-Logik)

Diese Checkliste wird pro analysierter Seite/Domain durchlaufen. Bewertung je Kategorie:
🟢 = erfüllt, 🟡 = teilweise/Optimierungspotenzial, 🔴 = kritischer Mangel.

Eine Kategorie ist automatisch 🔴, wenn eines ihrer "K.O."-Kriterien verletzt ist.

## Kategorie A: Crawling & Indexierung (K.O.-Kategorie)

- [ ] Seite liefert HTTP 200 (kein 4xx/5xx) – **im Antwortkopf gemessen, nicht am Inhalt
      abgelesen** (R-TECH-006): Status, `x-robots-tag`, `retry-after` je Seitentyp; eine
      nicht vorhandene Adresse liefert 404
- [ ] Kein versehentliches `noindex` oder robots.txt-Block auf wichtigen Seiten
- [ ] robots.txt vorhanden, sperrt keine wichtigen Bereiche versehentlich
- [ ] XML-Sitemap vorhanden und aktuell, in robots.txt referenziert
- [ ] Kanonische URL (`rel=canonical`) gesetzt und korrekt (verweist auf sich selbst bzw. die
      bevorzugte Version bei Duplikaten)
- [ ] Interne Verlinkung: wichtige Seiten sind max. 3–4 Klicks von der Startseite entfernt
- [ ] Kein Duplicate-Content-/Keyword-Kannibalisierungs-Risiko zwischen mehreren eigenen Seiten
      zum gleichen Thema

## Kategorie B: Content & E-E-A-T

- [ ] Klar erkennbarer Nutzen/Zweck des Inhalts für eine echte Zielgruppe (nicht nur für Google)
- [ ] Original­ität: eigene Einordnung/Erfahrung/Daten statt reiner Zusammenfassung fremder
      Quellen
- [ ] Autor:innenschaft erkennbar, bei YMYL-Themen mit nachvollziehbarer Fachexpertise
- [ ] Aktualität erkennbar (Datum, Aktualisierungshinweis) bei zeitkritischen Themen
- [ ] Quellenangaben/Belege bei Fakten, Statistiken, Studienbezügen
- [ ] Title-Tag: enthält Haupt-Keyword, ist einzigartig, ca. 50–60 Zeichen, für Menschen
      verständlich (kein reines Keyword-Stapeln)
- [ ] Meta-Description: prägnant, klickfördernd, ca. 150–160 Zeichen, spiegelt Seiteninhalt
      wahrheitsgemäß
- [ ] H1 vorhanden und thematisch stimmig mit Title; benennt sie das Seitenthema so,
      dass sie auch als Ergebniszeile in der Suche taugen würde? (R-HEAD-010, R-HEAD-012)
- [ ] Zwischenüberschriften benennen ihr Thema, statt es nur anzudeuten – Prüfkriterium
      ist Verständlichkeit, nicht Keyword-Vorkommen (R-HEAD-020)
- [ ] Bei mehreren verwandten Seiten der Domain: keine wortgleichen H2 über die Seiten
      hinweg (R-HEAD-023)
- [ ] H-Hierarchie ohne Sprünge – als Barrierefreiheits-Kriterium bewertet, nicht als
      Rankingkriterium (R-HEAD-002)
- [ ] Kein Keyword-Stuffing, keine unnatürliche Wiederholung von Phrasen
- [ ] Absätze/Struktur für Leser:innen und Featured-Snippet-/KI-Zitierfähigkeit optimiert
      (prägnante Antwort direkt nach Zwischenüberschrift, wo thematisch passend)

## Kategorie C: Page Experience & Core Web Vitals

- [ ] LCP ≤ 2,5 s (mobil und Desktop, laut PageSpeed-Insights-Live-Check)
- [ ] INP ≤ 200 ms
- [ ] CLS ≤ 0,1
- [ ] HTTPS durchgängig, keine Mixed-Content-Warnungen
- [ ] Mobile Darstellung funktional (Viewport, Touch-Ziele, Lesbarkeit ohne Zoom)
- [ ] Keine aufdringlichen Interstitials/Pop-ups, die Content verdecken
- [ ] Hauptinhalt visuell klar von Werbung/Nebeninhalt abgegrenzt
- [ ] Cookie-/Consent-Banner blockiert nicht Rendering oder Crawling wichtiger Inhalte

## Kategorie D: Strukturierte Daten

- [ ] Passendes Schema-Markup vorhanden (Article, Product, FAQ, LocalBusiness, Breadcrumb etc.
      je nach Seitentyp)
- [ ] Alle Pflichtfelder des jeweiligen Typs ausgefüllt
- [ ] Markup entspricht wahrheitsgemäß dem sichtbaren Inhalt (keine Fake-Bewertungen)
- [ ] Keine Blockierung der strukturierten Daten durch robots.txt/noindex

## Kategorie E: Spam-Risiko-Check (sollte durchgängig 🟢 sein – jeder Treffer ist ein Alarm)

- [ ] Kein Cloaking erkennbar
- [ ] Keine Doorway-Seiten-Muster
- [ ] Keine gekauften/unnatürlichen Linkmuster erkennbar (soweit einsehbar)
- [ ] Keine massenhaft, erkennbar unredigiert KI-generierten Texte ohne Mehrwert
- [ ] Keine versteckten Texte/Links

## Kategorie F: KI-Suche/GEO-Fitness

- [ ] Inhalte beantworten konkrete Nutzerfragen direkt und prägnant (zitierfähig für AI
      Overviews/Featured Snippets)
- [ ] Klare Attribution/Autor:innenschaft (wichtig für KI-Quellenverweise)
- [ ] Themen-Tiefe/Vollständigkeit statt oberflächlicher Rundum-Artikel ohne Substanz
- [ ] llms.txt vorhanden und sinnvoll konfiguriert (optional, noch kein offizieller Standard –
      als "nice to have", nicht als Pflichtkriterium bewerten)

## Gesamtbewertung ableiten

- **🔴 Gesamt**, wenn Kategorie A (Crawling/Indexierung) 🔴 ist – ohne Indexierung ist alles
  andere irrelevant.
- **🟡 Gesamt**, wenn Kategorie A 🟢/🟡, aber B oder E deutliche Mängel zeigen.
- **🟢 Gesamt**, wenn A–E überwiegend 🟢 sind und höchstens einzelne 🟡 in C/D/F bestehen.
