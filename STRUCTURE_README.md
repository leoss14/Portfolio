# Portfolio File Structure

## Overview

All project files follow a standardized directory layout. Shared assets (CSS, JS) are centralized, and each project is self-contained under `projects/`.

## Directory Layout

```
Website-/
├── index.html                  Landing page
├── about.html                  About page
├── contact.html                Contact page
├── projects.html               Project listing page
├── favicon.svg
│
├── css/
│   ├── style.css               Global styles
│   └── project-shared.css      Shared styles across project pages
│
├── js/
│   └── nav.js                  Navigation scroll behavior
│
├── projects/
│   ├── capstone/
│   │   ├── page.html           Project write-up
│   │   ├── code/               Notebooks (.ipynb)
│   │   └── outputs/            Visualizations (cluster/, ml/)
│   │
│   ├── central-bank/
│   │   ├── page.html
│   │   ├── code/
│   │   ├── data/               FRED CSVs (FEDFUNDS, CPI, etc.)
│   │   └── outputs/            PNGs (regime charts, Taylor rule, etc.)
│   │
│   ├── pink-tax/
│   │   ├── page.html
│   │   ├── code/
│   │   └── outputs/            charts/ (regression, validation, ML pipeline)
│   │
│   ├── uber/
│   │   ├── page.html
│   │   ├── code/
│   │   ├── data/               Parquets, shapefiles, GeoJSON
│   │   └── outputs/            Interactive HTML maps and charts
│   │
│   └── export/
│       ├── data/               Atlas trade data (.dta)
│       └── outputs/            PNGs, treemaps, opportunity CSVs
│
├── all-pages/                  Symlinks to all HTML pages (convenience)
└── .gitignore                  Excludes large data files from git
```

## Path Conventions

From root pages (`index.html`, `about.html`, etc.):
- CSS: `css/style.css`
- JS: `js/nav.js`
- Project pages: `projects/<name>/page.html`
- Project outputs: `projects/<name>/outputs/...`

From project pages (`projects/<name>/page.html`):
- CSS: `../../css/style.css`, `../../css/project-shared.css`
- JS: `../../js/nav.js`
- Navigation: `../../index.html`, `../../projects.html`, etc.
- Own outputs: `outputs/...` (relative to project folder)

## Data Files

Large data files (`.parquet`, `.dta`, `.shp`, `.geojson`) are kept locally in each project's `data/` folder but excluded from git via `.gitignore`.

## Adding a New Project

1. Create `projects/<project-name>/` with `page.html`, `code/`, `data/`, `outputs/`
2. Use `../../css/style.css` and `../../js/nav.js` in the page header
3. Reference outputs with relative paths (`outputs/...`)
4. Add a card in `projects.html` linking to `projects/<project-name>/page.html`
5. Add a symlink: `ln -s ../projects/<project-name>/page.html all-pages/<project-name>.html`
