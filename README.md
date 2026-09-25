# Jimmy Liu — Portfolio

Personal portfolio / resume site. Single-page, dependency-free HTML + CSS.

**Live site:** https://jimmycode888.github.io/portfolio/

## Contents

| File | Purpose |
| --- | --- |
| `index.html` | The entire site (markup + inline CSS, no build step) |
| `.nojekyll` | Tells GitHub Pages to serve files as-is, skipping Jekyll processing |

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
