# Brutalist — design reference

**Acid yellow and thick borders**

One page showing every component in this design, rendered from its own design
tokens. No build step, no dependencies: open `index.html`.

**[View the component gallery →](https://mawentory.github.io/design-brutalista/)**

![Brutalist](preview.png)

## What is here

| File | Purpose |
| --- | --- |
| `index.html` | Component gallery — every component on one page |
| `DESIGN.md` | The design notes: origin, palette, type, shape, measured contrast |
| `theme.css` | The 66 design tokens, plus derived accessibility values |
| `design.css` | Component styles, written against tokens only |
| `fonts.css` | `@font-face` declarations for the fonts this design uses |
| `fonts/` | Latin-subset woff2 files, self-hosted |

`design.css` contains no colour, radius or font literal. That is deliberate: the
same stylesheet drives all ten designs and only `theme.css` differs, so the
gallery doubles as a test that the token set is complete.

## The design

Web brutalism: raw structure left visible, acid yellow ground, and 4px black borders that refuse to be subtle.

**Type** — Inter for body text and Archivo Black at its single weight of 400 for display — the heaviest available face, used exactly as shipped.

**Shape** — Zero radii. Square corners everywhere, including switches and radio dots, with 10px 10px 0 hard shadows.

**Signature moves**

- Every corner square, including toggles and choice dots.
- 4px borders and hard offset shadows.
- Thick band under the sticky header.

## Colour

| Token | Value | Role |
| --- | --- | --- |
| `--paper` | `#e8ff59` | Page ground |
| `--sheet` | `#ffffff` | Raised surfaces |
| `--ink` | `#0a0a0a` | Primary text |
| `--signal` | `#ff2d6f` | Action |
| `--signal-text` | `#cb2459` | Action, when it has to be read |
| `--focus-ring` | `#ff2d6f` | Focus indicator |

## Accessibility

Every colour pair this design can render as text is checked against WCAG 2.1
when the repo is generated — page surfaces, panel surfaces, and the tinted fills
of badges and diff lines. The full table is in
[DESIGN.md](DESIGN.md#contrast-measured); the gallery is separately audited in a
real browser for heading order, duplicate ids, unlabelled controls and
horizontal overflow at 1280px and 390px.

## Using it

Set the theme attribute on your root element and load the two stylesheets:

```html
<html data-theme="brutalista">
  <link rel="stylesheet" href="fonts.css" />
  <link rel="stylesheet" href="theme.css" />
  <link rel="stylesheet" href="design.css" />
</html>
```

Because the tokens are namespaced by attribute, this theme can sit alongside
another one in the same page.

## The rest of the set

[Placa](https://github.com/mawentory/design-placa), [Blueprint](https://github.com/mawentory/design-blueprint), [Phosphor](https://github.com/mawentory/design-fosforo), [Press](https://github.com/mawentory/design-imprensa), [Swiss](https://github.com/mawentory/design-suico), [Neon](https://github.com/mawentory/design-neon), [Botanical](https://github.com/mawentory/design-botanico), [Bauhaus](https://github.com/mawentory/design-bauhaus), [Vidro](https://github.com/mawentory/design-vidro).

---

Part of the MarvinRouter design set. Generated from a single template; see
`DESIGN.md` for the values behind it.
