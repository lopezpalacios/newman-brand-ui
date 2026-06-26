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
docs/                   # brandbook.html · BRAND.md · DESIGN.md (Stitch format)
prompts/                # reusable agent prompts (devibe-review.md)
.github/workflows/      # GitHub Pages deploy
```

## Run locally
```bash
npm start          # → http://localhost:8000   (python3 -m http.server)
```
No build step. No runtime dependencies. Plain HTML/CSS/JS. See [`CONTRIBUTING.md`](./CONTRIBUTING.md).

## Design notes
Committee-audited for a 10/10 bar, then refined with **T1 Energy restraint lessons** (Newman colors kept):
- **Whisper-light display** — headlines at weight 300, line-height ~1.0, open `.01em` tracking. Architectural, not shouted.
- **Square section-label** — every kicker is prefixed by a 4–6px solid magenta square (machined dial, not a bullet).
- **Generous rounding** — pills/buttons 100px, image portholes 64px, cards 24px, floating pill nav 16px.
- **Flat & shadowless** — hierarchy via tonal layering (paper → white → carbon → onyx) + spacing, not elevation.
- **Gradient demoted to the ~1% accent** — brand bar, one hero word, primary button, isotype, label squares only.
- **4px-base spacing rhythm**, ~48px section gaps, comfortable density.
- **OKLCH gradient interpolation** (sRGB fallback) removes the muddy plum mid-band.
- **Contrast-safe magenta** (`--magenta-ink #8A0A4B`) for text; gradient never under body copy.
- **Accessibility:** skip link, `:focus-visible` rings, ARIA tabs/modal, `prefers-reduced-motion` guard; print flattens gradients.

## License
Brand assets © Newman. Code MIT.
