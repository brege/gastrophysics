---
title: "What is Pesto?"
summary: "A short pesto note and a recipe-template example."
tags:
  - pesto
  - basil
  - sauce
  - mediterranean
  - olive-oil
  - garlic
  - herbs
categories:
  - culinary
date: 2022-12-11T16:56:56-05:00
draft: false
ShowToc: true
math: true
homeLead: true
cover:
  image: cover.svg
  alt: "Diagram of herbs, oil, garlic, nuts, and cheese converging into pesto"
  caption: "Pesto as a small sauce graph."
---

**Pesto\*** is a cold-prep green sauce made with herbs and alliums suspended in oil. Most pestos call for some form of nut or cheese. In the general sense, chefs may specify "loose pesto" when there are neither cheese nor nuts in the sauce, or when the sauce has an abundance of oil. In general, pesto is made from herbs in the mint family, almost always from basil. The **\*** distinguishes a generalization to the traditional meaning of the word.

## Recipe Template

The `recipe` shortcode wraps a recipe body in the theme's recipe card.
Use ordinary Markdown inside the shortcode so the recipe remains readable
in source form.

```go-html-template
{{%/* recipe */%}}

## Basil Pesto

**Chef:** Gastrophysics Demo

**Yield:** 1 Quart

### Ingredients

- 2 bunch basil
- 8-10 cloves peeled garlic
- 3 cups extra virgin olive oil
- 1/4 cup seasonal tree nuts
- 1/4 cup grated parmesan
- salt and black pepper

### Directions

Puree everything except the parmesan, then fold in the cheese.

{{%/* /recipe */%}}
```

The same template is used by [Basil Pesto](/recipes/basil-pesto/), [Pesto Aioli](/recipes/pesto-aioli/), and [Chicken Salad](/recipes/chicken-salad/).

## Pesto Grammar

In the minimum useful sense, pesto behaves like a small graph of green
ingredients, fat, allium, texture, and optional dairy:

$$
\textrm{pesto} \approx \textrm{herbs} + \textrm{oil} + \textrm{allium} + \textrm{texture} + \textrm{salt}
$$
