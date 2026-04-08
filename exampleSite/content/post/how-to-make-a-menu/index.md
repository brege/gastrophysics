---
title: "How to Make a Menu"
summary: "A menu-template note for the Gastrophysics menu shortcode."
tags:
  - menus
  - pesto
  - farmers-market
  - seasonal
categories:
  - culinary
date: 2022-12-18T11:00:00-05:00
draft: false
ShowToc: true
cover:
  image: cover.svg
  alt: "Diagram of farmer's market produce moving through menu courses"
  caption: "A menu as a compact seasonal flow."
---

A menu page is a dated bundle with `type: menus`. The `menu` shortcode
wraps a short sequence of courses and uses the page date and site author
in the menu footer.
For a full menu page, you can also write plain Markdown in a page with
`type: menus` and let the layout render the card and footer.

```go-html-template
{{%/* menu */%}}

## Farmer's Market Menu

### Basil Pesto Pasta

linguini, zephyr squash, heirloom cherry tomatoes,
spinach, feta cheese, creamy pesto sauce

### Peach Crepes

blueberry whipped cream, pumpkin seed brittle

{{%/* /menu */%}}
```

The example menu archive keeps menus as their own top-level section:
[October 18, 2018](/menus/2018-10-18-farmers-market-menu/)
and [August 1, 2019](/menus/2019-08-01-farmers-market-menu/).
