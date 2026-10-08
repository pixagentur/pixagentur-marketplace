# Schreibstil treffen & natürlich klingende Texte erzeugen

Ziel: Neue/geänderte Textpassagen sollen (a) zum bestehenden Schreibstil der Seite passen und
(b) sich wie von einer erfahrenen menschlichen Fachperson geschrieben lesen – nicht wie
generischer, austauschbarer KI-Text. Das ist kein Trick gegen Google, sondern deckt sich mit
Googles eigener Anforderung an "people-first"-Content mit echter Erfahrung/Expertise (E-E-A-T,
siehe `01-google-regeln.md`): auffällig generischer KI-Text wirkt unspezifisch und wenig
vertrauenswürdig – für Leser:innen wie für Googles Systeme.

## Schritt 1: Stil-Fingerabdruck des Originaltexts erstellen

Vor dem Schreiben neuer Texte den vorhandenen Text kurz analysieren und stichpunktartig
festhalten (nicht im finalen Report ausbreiten, nur als interne Arbeitsgrundlage):

- **Anrede**: Du/Sie/neutral? Wird gegendert (z. B. Doppelpunkt, Sternchen, neutral)?
- **Satzlänge & Rhythmus**: Eher kurze, prägnante Sätze oder komplexe Schachtelsätze?
- **Fachjargon-Level**: Laienverständlich oder Fachpublikum?
- **Tonalität**: Sachlich-nüchtern, verkäuferisch-emotional, humorvoll, autoritär-beratend?
- **Typische Satzanfänge/Wendungen** der Marke (z. B. immer wiederkehrende Formulierungen,
  Claims, Call-to-Actions).
- **Absatzlänge und Struktur** (kurze Absätze vs. Fließtext, Nutzung von Aufzählungen).

Neue Textvorschläge müssen zu diesem Fingerabdruck passen – nicht zu einem generischen
"neutralen Business-Deutsch".

## Schritt 2: Typische KI-Textmuster vermeiden

Folgende Muster wirken generisch und sollten in den Neu-Texten konsequent vermieden werden:

- Abgenutzte Einleitungsfloskeln ("In der heutigen schnelllebigen Welt...", "Es ist wichtig zu
  betonen, dass...", "Nicht zu unterschätzen ist...")
- Übermäßig gleichförmiger Satzbau (viele Sätze mit identischer Länge/Struktur hintereinander)
- Aufzählungs-Inflation, wo ein normaler Fließtext natürlicher wäre
- Inhaltsleere Zusammenfassungssätze am Absatzende ("Zusammenfassend lässt sich sagen...")
- Übertriebene Aufzählung von Adjektiven/Superlativen ohne Beleg ("hochmodern, innovativ,
  zukunftsweisend")
- Generische Übergangsfloskeln in jedem zweiten Satz ("Darüber hinaus", "Außerdem",
  "Nichtsdestotrotz") – sparsam und variiert einsetzen
- Austauschbare Aussagen, die für jede beliebige Branche/jedes Produkt gelten könnten, statt
  konkreter, spezifischer Aussagen zum tatsächlichen Angebot

## Schritt 3: Konkrete Mittel für natürlich wirkenden, glaubwürdigen Text

- **Variation**: Satzlängen bewusst mischen (kurz, dann länger, dann wieder kurz).
- **Konkretion statt Behauptung**: Statt "hohe Qualität" lieber ein konkretes Detail, ein Beispiel,
  eine Zahl oder Erfahrung nennen (mit den Kund:innen abstimmen, keine Fakten erfinden).
- **Aktive, spezifische Sprache** statt Passiv- und Nominalstil-Häufung.
- **Echte Perspektive einbauen**, wo möglich: Erfahrungswerte, Kund:innen-Nutzen, konkrete
  Anwendungsfälle statt abstrakter Beschreibungen.
- **Rhetorische Unregelmäßigkeit**: nicht jeder Absatz muss gleich aufgebaut sein (nicht immer
  Einleitungssatz → 3 Bulletpoints → Fazitsatz).
- Ein bis zwei Ecken/Kanten zulassen (z. B. eine pointierte Meinung, ein kritischer Nebensatz) –
  das macht Text menschlicher als durchgängig glatte Zustimmung.

## Schritt 4: Qualitätscheck vor Auslieferung

Vor dem Eintragen in die Text-Swap-Liste kurz prüfen:
1. Klingt das wie die Marke selbst schreiben würde (Stil-Fingerabdruck aus Schritt 1)?
2. Enthält der Text mindestens ein konkretes, spezifisches Element (kein reiner Textbaustein)?
3. Wurden keine Fakten/Zahlen/Erfahrungen erfunden, die nicht vom Kunden bestätigt wurden? Falls
   ein konkretes Detail fehlt, das den Text besser machen würde: als offene Frage an den Nutzer
   kennzeichnen statt zu erfinden.
4. Ist der Text weiterhin SEO-sauber (Ziel-Keyword natürlich integriert, keine Keyword-Stuffing)?

## Was die Stilregeln leisten und was nicht

Die Schritte 1 bis 4 machen einen Text lesbarer, halten die Markenstimme und vermeiden
erkennbar generische Werbesprache, und zwar für menschliche Leser:innen. Das ist ihr Zweck.

Sie leisten **nicht**, dass ein trainierter Klassifikator (KI-Detektor) den Text als
menschlich einstuft. Die Merkmalsliste ist aus der Beschreibung maschineller Texte
abgeleitet, nicht gegen das Urteil eines Detektors geprüft. Ein bestandener Selbsttest
(keine Floskel gefunden, Satzlängen gemischt) misst nur, ob die Liste eingehalten wurde.
Beobachtet: Ein Text, der jede Regel nachweislich einhielt, bekam von zwei schwachen
Detektoren 0 % und 12 %, vom stärksten 100 % maschinell; eine absichtlich im
Werkstattton umgeschriebene Fassung ebenfalls 100 %, ein nachweislich von Hand
geschriebener Text desselben Kunden 37 %.

Daraus folgt:

- „Nicht als KI-generiert erkennbar" wird weder versprochen noch als geprüfte Eigenschaft
  eines Textes ausgegeben, weder im Chat noch im Report.
- **Wird eine Prüfung auf maschinelle Herkunft verlangt**, läuft sie gegen echte Werkzeuge:
  mindestens zwei Detektoren unterschiedlicher Stärke, dazu eine Gegenprobe an einem
  gesichert von Hand geschriebenen Text derselben Quelle (gleicher Kunde, gleiche
  Textsorte). Berichtet werden alle drei Werte nebeneinander. Ohne Gegenprobe ist ein
  Prozentwert nicht interpretierbar: Stuft der Detektor auch den Handtext hoch ein, trennt
  er bei dieser Textsorte nicht.
- Für die Google-Bewertung spielt die Erstellungsmethode keine Rolle (R-CONTENT-040),
  entscheidend ist die Qualität. Ein Detektorwert ist deshalb kein SEO-Befund und fließt
  nicht in den Score ein.

## Hinweis

Diese Vorgaben dienen dazu, hochwertigen, glaubwürdigen und für Menschen wie Suchmaschinen
überzeugenden Content zu erzeugen. Sie ersetzen keine fachliche/juristische Prüfung bei
sensiblen (YMYL-)Inhalten und keine finale Freigabe durch den Auftraggeber vor Veröffentlichung.
