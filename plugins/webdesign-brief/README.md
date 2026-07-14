# webdesign-brief-skill

**Version:** 1.1.1 · **Autor:** [pixagentur](https://pixagentur.de) · [Changelog](CHANGELOG.md)

Claude-Skill von [pixagentur](https://pixagentur.de): ein verpflichtendes Intake-Briefing, das vor jedem neuen Webdesign-Auftrag (neue Webseite, Landingpage, Redesign) automatisch greift und Branche, Kunde, Farben, Hero-Layout, Animationen, Hintergrund, Bildmaterial, Referenzen, Tech-Stack, Umfang, Conversion-Ziel und Sprache abfragt — bevor irgendein Design oder Code entsteht.

## Installation

### Claude Code (Marketplace)

```
/plugin marketplace add pixagentur/webdesign-brief-skill
/plugin install webdesign-brief@webdesign-brief-skill
```

Oder über die Einstellungen: `Verzeichnis → Plugins → Aus einem Repository hinzufügen` und diese Repo-URL eintragen.

### Manuell (Claude Code, ohne Marketplace)

Ordner `skills/webdesign-brief/` nach `~/.claude/skills/webdesign-brief/` kopieren.

### claude.ai Chat/Design

`skills/webdesign-brief/` als Zip packen und über **Customize → Skills → Hinzufügen** hochladen (siehe Hinweis unten zu Claude Design).

## Inhalt

- `SKILL.md` — Trigger-Bedingungen, Pflicht-Intake-Fragenkatalog (A–L), Prozessablauf
- `references/farbe-typografie.md` — Farbrollen-System (60-30-10), Typografie/Type-Scale
- `references/layout-a11y.md` — Grid/Spacing/Hierarchie/Responsive/WCAG AA
- `references/conversion-seo.md` — Conversion-Bausteine, SEO-Komponenten
- `references/quellen-tools.md` — Inspirationsquellen, Higgsfield-Medienerstellung, verwandte Skills

## Bekannte Einschränkung

Claude Design (claude.ai/design) hat ein eigenes, fest verdrahtetes Skill-Menü ohne Unterstützung für Custom-Skills — dieser Skill greift dort aktuell nicht automatisch. Funktioniert zuverlässig in Claude Code und normalem claude.ai Chat.
