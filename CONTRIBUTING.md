# Contributing

## Project shape
Static, dependency-free site — plain HTML/CSS/JS. No build step.

```
index.html              # landing page (root — required by GitHub Pages)
assets/css/newman.css   # tokens + components
assets/js/newman.js     # behavior (IIFE, exposes window.Newman)
docs/                   # brand books: brandbook.html, BRAND.md, DESIGN.md
prompts/                # reusable agent prompts (e.g. devibe-review.md)
.github/workflows/      # Pages deploy
```

## Run locally
```bash
npm start          # python3 -m http.server 8000  → http://localhost:8000
```

## Conventions
- **Tokens first.** No hard-coded hex or magic numbers in components — use the CSS custom
  properties in `assets/css/newman.css`. New values get a token.
- **Source of truth:** [`docs/DESIGN.md`](docs/DESIGN.md) (Google Stitch format). Code must
  match it; if you change a token, update DESIGN.md in the same PR.
- **Accessibility is non-negotiable:** semantic landmarks, ARIA on interactive widgets,
  `:focus-visible` rings, `prefers-reduced-motion` guard. Don't regress them.
- **Brand rules:** gradient is the ~1% accent and never under body text; magenta text only
  via `--magenta-ink`; display headlines stay weight 300; flat/shadowless.
- **Format before commit:** `npm run format`.

## Commits
Conventional Commits (`feat:`, `fix:`, `docs:`, `refactor:`, `chore:`). Imperative subject,
≤72 chars.
