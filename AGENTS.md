# AGENTS.md

## Cursor Cloud specific instructions

This is a **zero-dependency static HTML portfolio/CV website** (`cv.html`). There is no build system, no package manager, and no framework.

### Running the site

Serve the file with any static HTTP server:

```bash
python3 -m http.server 8080
```

Then open `http://localhost:8080/cv.html` in a browser.

### Key notes

- The entire application is a single file: `cv.html` with inline CSS and JS.
- No linting, testing, or build tooling is configured in this repository.
- The `.gitignore` contains Angular/Node patterns but there is no Angular project; it's vestigial.
- External CDN dependencies: Google Fonts (Inter) and Material Icons — page still renders without network but with fallback fonts.
- Theme state is persisted in `localStorage` under key `bl-theme`.
- The page references `assets/cv/bogdan-levishchev-cv.pdf` and `assets/og-preview.png` which are not present in the repo (download buttons will 404).
