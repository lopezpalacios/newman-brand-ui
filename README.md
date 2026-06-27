# Newman — Brand Guidelines & UI Kit

Brand identity system and dependency-free UI kit for **Newman · Soluciones en Energía** — an energy
platform financing and commercializing solar generation and behind-the-meter storage across Mexico
and Latin America.

🔗 **Live:** https://lopezpalacios.github.io/newman-brand-ui/
🎨 **Brandbook:** [`docs/brandbook.html`](./docs/brandbook.html) (V1.0 — 2026)
📐 **Guidelines:** [`docs/BRAND.md`](./docs/BRAND.md) · [`docs/DESIGN.md`](./docs/DESIGN.md) (Google Stitch format, machine-readable)

## Structure
```
index.html              # landing page (root — required by GitHub Pages)
assets/css/newman.css   # tokens + accessible components (vanilla CSS)
assets/js/newman.js     # nav, ARIA tabs, focus-trap modal, toast, reveal, accordion, count-up, validation
assets/img/             # logo SVG/PNG exports, og-image.jpg, icon-*.png
favicon.* · apple-touch-icon.png · site.webmanifest
docs/                   # brandbook.html · BRAND.md · DESIGN.md (Stitch format)
prompts/                # reusable agent prompts (devibe-review.md)
.github/workflows/      # GitHub Pages deploy
```

## Run locally
```bash
npm start          # → http://localhost:8000   (python3 -m http.server)
```
No build step. No runtime dependencies. Plain HTML/CSS/JS. See [`CONTRIBUTING.md`](./CONTRIBUTING.md).

## Design notes (v3 — light, purple-forward, flat)
Color-committee audited; every text/background pair passes WCAG AA (most AAA).
- **Light warm-lilac canvas** `#F6F4F9`, deep-aubergine text `#221A33` (15:1) — no more dark slabs.
- **One solid brand purple** `#621558` does all accent work (buttons, links, rules, stats). **No chrome gradients** — the navy→magenta gradient lives only inside the logo isotype.
- **Navy `#191B4D`** anchors headlines + the single dark surfaces (nav pill, footer).
- **Magenta `#B80E65`** survives only as the 4px section-label square.
- **Whisper-light display** (Montserrat 300, ~1.0 line-height), **4px square labels**, **generous rounding** (pills 100px, portholes 64px, cards 24px), **flat & shadowless** tonal layering, 4px spacing rhythm.
- **Accessibility:** skip link, `:focus-visible` rings, ARIA tabs/modal, `prefers-reduced-motion`.
- Full token spec + contrast table: [`docs/DESIGN.md`](./docs/DESIGN.md).

## Brand assets
`favicon.svg`, `favicon.ico` (16/32/48/64), `apple-touch-icon.png` (180), `site.webmanifest`
(192/512 + maskable), social `assets/img/og-image.jpg` (1200×630), and logo exports
(`assets/img/logo-lockup.svg` · `logo-isotype.svg` · `logo-lockup.png`).

## License
Brand assets © Newman. Code MIT.
