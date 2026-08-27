# tahvia127.github.io

My portfolio, served at **<https://tahvia127.github.io>**.

A static site — no build step, no dependencies. Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

## Structure

```
index.html          Single-page portfolio — hero, work grid, about, contact
styles.css          Design system and layout for the landing page
project-*.html      16 individual project case studies
project-styles.css  Shared styles for the case-study pages
photos/             Project imagery (WebP)
fonts/              Aileron and Medino typefaces
```

## Design notes

- **Type:** Cormorant Garamond (display), Inter (body), Pinyon Script (wordmark), loaded from Google Fonts.
- **Palette:** warm paper `#FAF7F2`, ink `#17150F`, gold `#9A7830`, with sage/clay/slate accents on the toolkit chips.
- **Filtering** on the work grid is plain JavaScript toggling `hidden` — no framework.
- **Accessibility:** skip link, visible focus rings, `aria-pressed` on the filter controls, and full `prefers-reduced-motion` support.
- **Images** are WebP, capped at 1600px wide and lazy-loaded below the fold.

## Adding a project

1. Copy an existing `project-*.html` as a starting point.
2. Add a `<article class="card">` to the grid in `index.html` with a `data-cat` of `data`, `product`, or `design` — the filter picks it up automatically.
3. Put any imagery in `photos/` as WebP.
