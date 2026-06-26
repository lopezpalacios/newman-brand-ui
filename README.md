# Newman — Brand Guidelines & UI Kit

Brand identity system and dependency-free UI kit for **Newman · Soluciones en Energía** — an energy
platform financing and commercializing solar generation and behind-the-meter storage across Mexico
and Latin America.

🔗 **Live:** https://lopezpalacios.github.io/newman-brand-ui/
🎨 **Brandbook:** [`brandbook.html`](./brandbook.html) (V1.0 — 2026)
📐 **Guidelines:** [`BRAND.md`](./BRAND.md)

## Contents
| File | What |
|------|------|
| `index.html` | Reference landing page using the full kit |
| `newman.css` | Tokens + accessible components (vanilla CSS) |
| `newman.js` | Nav, ARIA tabs, focus-trapped modal, toast, reveal, accordion, count-up, form validation (zero deps) |
| `brandbook.html` | The 12-section visual + verbal identity book |
| `BRAND.md` | Quick-reference brand rules |

## Run locally
```bash
python3 -m http.server 8000   # then open http://localhost:8000
```
No build step. No dependencies. Plain HTML/CSS/JS.

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
