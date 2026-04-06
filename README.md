# Gastrophysics

A Hugo theme for people with split careers. It is print- and e-reader-friendly, with first-class support for sectional CVs, recipes, and tasting menus.

Demo: [brege.org](https://brege.org)

Started as a fork of [PaperMod](https://github.com/adityatelange/hugo-PaperMod/).

## Features

- Light/dark mode with automatic system detection
- 11 [color palettes](#color-palettes)
- Palette-aware syntax highlighting
- Sectional CV layout driven by `cv.yaml`
- Recipe and tasting menu shortcodes with archive views
- Balanced text wrapping for navigation and footer sequences
- Anchored headings with configurable depth
- Compact and expanded post card layouts
- Centralized SVG icon registry
- Search, RSS, Open Graph, Twitter Cards, and JSON-LD

## Color Palettes

You can mix and match palettes in `hugo.toml`:

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
- nordic-linen
- sepia

Syntax highlighting is palette-aware across all palettes.

## CV Module

See [layouts/cv/README.md](layouts/cv/README.md).

## Recipe/Menu Module

- `recipe`: renders structured recipe markup
- `recipe-list`: renders recipes from a subsection
- `menu`: renders a tasting menu card and pulls the author from page or site params
- `menu-list`: renders a menu archive with optional H3 preview extraction

## License

[MIT](LICENSE)
