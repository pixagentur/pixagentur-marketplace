# PIXAGENTUR Marketplace – Claude Code Plugins

Zentrale [Claude Code Plugin-Marketplace](https://docs.claude.com/en/docs/claude-code/plugins) von PIXAGENTUR mit allen intern entwickelten Skills.

## Installation

In Claude Code:

```
/plugin marketplace add pixagentur/pixagentur-marketplace
/plugin install seo-ranking-experte@pixagentur-marketplace
/plugin install webdesign-brief@pixagentur-marketplace
```

## Updates

Neue Versionen werden hier im Repo veröffentlicht. Damit installierte Kopien automatisch aktualisiert werden, Auto-Update für diese Marketplace einmalig aktivieren (`/plugin` → Marketplaces → `pixagentur-marketplace`). Ohne diese Einstellung: `/plugin marketplace update pixagentur-marketplace`.

## Enthaltene Plugins

| Plugin | Beschreibung |
|---|---|
| [`seo-ranking-experte`](./plugins/seo-ranking-experte/) | SEO-Audit, Score, Handlungsempfehlungen, Text-Swaps, automatischer PDF-Report |
| [`webdesign-brief`](./plugins/webdesign-brief/) | Verpflichtendes Intake-Briefing vor jedem Webdesign-Auftrag |
