# Gastrophysics

A Hugo theme for people of multiple careers. Print-friendly, reader-focused, with modules for CV/resume, recipes, and tasting menus.

Demo: [brege.org](https://brege.org)

Forked from [PaperMod](https://github.com/adityatelange/hugo-PaperMod/).

## Features

- Light/dark mode with automatic system detection
- 10 [color palettes](#color-palettes)
- Palette-aware syntax highlighting
- CV module with YAML data and multiple section handlers
- Recipe and tasting menu module with view toggles and archive
- Balanced text wrapping for navigation and footer
- Anchored headings with configurable depth
- Compact and expanded post card views with tag clamping
- Section-scoped post navigation
- Consolidated SVG icon registry
- Search, RSS, OpenGraph, Twitter Cards, JSON-LD

## Color Palettes

Set in `hugo.toml`:

```toml
[params]
  colorLight = 'linen'
  colorDark = 'nord'
```

- linen (my custom palette)
- [rose-pine](https://github.com/rose-pine/rose-pine-theme)
- [rose-pine-moon](https://github.com/rose-pine/rose-pine-theme)
- [catppuccin-frappe](https://github.com/catppuccin/catppuccin)
- [catppuccin-macchiato](https://github.com/catppuccin/catppuccin)
- [catppuccin-mocha](https://github.com/catppuccin/catppuccin)
- [nord](https://github.com/nordtheme/nord)
- [gruvbox](https://github.com/morhetz/gruvbox)
- [everforest](https://github.com/sainnhe/everforest)
- sepia

Additionally, appropriate code syntax highlighting is available for all of these palettes.

## CV Module

See [layouts/cv/README.md](layouts/cv/README.md).

## Recipe/Menu Module

- `recipe`: structured recipe markup
- `recipe-list`: lists recipes from a subsection
- `menu`: tasting menu card, pulls author from page/site params
- `menu-list`: menu archive with optional H3 preview extraction

## License

[MIT](LICENSE)
