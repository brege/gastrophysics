# CV Module

The CV page is a Hugo page bundle using the `cv` layout type.

## Files

Create the CV as a Hugo page bundle. The `index.md` file may contain only
front matter; `cv.yaml` is the CV source of truth.

- `index.md`: front matter for the CV page bundle
- `cv.yaml`: structured CV data, the primary source for the rendered page

The theme renders the styled CV, reader shadow, table of contents, search text,
RSS content, schema body, and CV word count from `cv.yaml`.

See [example](https://github.com/brege/brege.org/blob/master/content/cv/cv.yaml) for a full example.

## Front Matter

```yaml
title: Name
type: cv
ShowToc: true
TocOpen: false
tocStartLevel: 2
tocEndLevel: 2     # simple non-branching section list
headerNav: true    # enables sticky section navigation
navDepth: 3        # heading depth for the nav
hideCvKeyboardTip: false
```

## cv.yaml Schema

The top-level `intro` key is optional Markdown rendered before the CV sections.
The top-level `sections` key is a list of objects. Each section has:

| Field     | Required | Description                                    |
|-----------|----------|------------------------------------------------|
| `title`   | yes      | section heading (rendered as h2)               |
| `handler` | yes      | which partial renders the section              |
| `class`   | no       | CSS class added to the section container       |
| `items`   | yes      | list of entries, structure depends on handler   |
| `note`    | no       | markdown footnote rendered after items         |

### Handlers

**pairs**: labeled groups of linked entries (expertise, technologies)

```yaml
items:
  - label: computing
    entries:
      - name: data science
        url: https://...
        primary: true    # optional, highlights the entry
```

**rows**: compact date-content rows (professional, education, awards, memberships)

```yaml
items:
  - date: "2023"
    content: "**Title**, *Organization*, Location"
```

Dates can contain `|` delimiters for multiple terms (e.g., `"2017 | 2016 | 2015"`).

**detail**: expanded entries with full markdown content (publications, talks)

```yaml
items:
  - date: "2018"
    content: |-
      **Paper Title**

      Author list...

      [Journal reference](https://...)
```

**projects**: software project cards with stack tags and links

```yaml
items:
  - name: project-name
    url: https://...
    summary: >-
      one-line description
    stack: python, flask, docker
    links:
      - label: Source
        url: https://...
      - label: Demo
        url: https://...
```

**research**: research experience with title, meta, and bullet content

```yaml
items:
  - date: "May 2013 | to | Sep 2018"
    title: "Research topic"
    meta: "[Dept](https://...), [University](https://...)"
    content:
      - >-
        Description paragraph with [links](https://...).
```

**teaching**: course listings with code, kind, and detail links

```yaml
items:
  - date: "S-2012 | F-2010"
    code: PHYS 101
    kind: Laboratory
    name: General Physics I
    tag: optional note
    detail:
      - name: topic
        url: https://...
```

Date prefixes: `S-` (spring), `F-` (fall), `X-` (summer).
