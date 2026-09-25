# Jimmy Liu — Portfolio

Personal portfolio / resume site. Single-page, dependency-free HTML + CSS.

**Live site:** https://jimmycode888.github.io/portfolio/

## Contents

| File | Purpose |
| --- | --- |
| `index.html` | The entire site (markup + inline CSS + a little vanilla JS, no build step) |
| `assets/Jimmy_Liu_CV.pdf` | The CV served by the Download CV buttons |
| `.nojekyll` | Tells GitHub Pages to serve files as-is, skipping Jekyll processing |

## Theme

Light and dark palettes are defined once as CSS custom properties on `:root`, so every
colour in the stylesheet resolves through a variable — there are no hardcoded colours in
component rules.

- On first visit the theme follows the operating system (`prefers-color-scheme`).
- Clicking the nav toggle stores an explicit choice in `localStorage` under `theme`,
  which then wins over the OS.
- A small inline script in `<head>` resolves the theme *before* first paint, so there is
  no flash of the wrong palette.
- The toggle swaps its sun/moon icon and keeps `aria-label` / `title` / `theme-color`
  in sync.

To force a palette for testing, set `data-theme="dark"` or `data-theme="light"` on the
`<html>` element.

## Updating the CV

The Download CV buttons point at `assets/Jimmy_Liu_CV.pdf`. Replace that file with a new
export and push — the buttons pick it up automatically.

## Sections

About · Experience · Trade Ambassador Programme · Selected Projects · Skills & Passions · Education & Certifications · Exchange Experience · Contact

## Local preview

Open `index.html` directly in a browser, or serve the folder:

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

## Deployment

Served by GitHub Pages from the `main` branch root. To update the site, edit `index.html`, commit, and push:

```bash
git add -A
git commit -m "Update portfolio content"
git push
```

Changes go live within roughly a minute.
