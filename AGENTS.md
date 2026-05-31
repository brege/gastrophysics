# Gastrophysics Theme

Hard fork of PaperMod.

## Two-layer override system

Hugo merges site-level files over theme files. Both layers are active:

- **Theme** (`themes/gastrophysics/`): layouts, CSS, shortcodes, i18n
- **Site** (repo root): content, config, site-specific layout overrides, site-specific CSS

## CSS cascade

Concatenated in `head.html`:

1. **core** (theme-vars, reset, common/*, chroma, includes, media queries)
2. **palette** (11 color palettes, syntax token colors, typography/fonts)
3. **components** (~16 files split by UI component)
4. **extended** (user override hook; theme ships only `blank.css`)

The `extended/` directory is the override contract: `resources.Match "css/extended/*.css"` merges theme and site assets. Theme CSS must not live in `extended/`.

## Palette system

Color palettes are configured in `hugo.toml` via `color`, `colorLight`, and `colorDark`, then emitted on `<html>` as `data-theme-palette`, `data-theme-palette-light`, and `data-theme-palette-dark`. For available palette names, see the README or `assets/css/palette/colors.css`.

## Partials

```
partials/
  head.html, header.html, footer.html, extend_head/footer.html
  svg.html, cover.html, author.html, social_icons.html
  post/        single_meta, nav_links, edit, share, anchored_headings
  home/        info, markers, roles
  nav/         breadcrumbs, sections, series, toc
  recipe/      view_toggle, wrap
  cv/          YAML-backed CV renderers
  menu/        card
  tags/        rail
  vendor/      katex, jquery
  util/        balanced_sequence, balancer_script
  templates/   opengraph, twitter_cards, schema_json
```

## Content types

| Type      | Layout                | Section path |
|-----------|-----------------------|--------------|
| post      | `_default/single.html` | /post/       |
| post list | `_default/list.html`   | /post/, home |
| recipe    | `recipes/list.html`    | /recipes/    |
| menu      | `menus/list.html`      | /menus/      |
| cv        | `cv/single.html`       | /cv/         |
| search    | `_default/search.html` | /search/     |

## Shortcodes

`menu`, `menu-list`, `recipe`, `recipe-from`, `recipe-list`, `kbd-tip`, `codefile`, `figure`

## Balanced sequence

`util/balanced_sequence.html` + `util/balancer_script.html`: flex-wrap layout with separator characters, configured via `--balanced-*` CSS properties.

## CV Module

See [layouts/cv/README.md](layouts/cv/README.md).
