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
This build was audited against a panel of design/frontend critiques and corrected for a 10/10 bar:
- **OKLCH gradient interpolation** (with sRGB fallback) removes the muddy plum mid-band.
- **Contrast-safe magenta** (`--magenta-ink #8A0A4B`) for text; the gradient never sits under body copy.
- **Accessibility:** skip link, `:focus-visible` rings, ARIA tabs/modal, `prefers-reduced-motion` guard.
- **Print/email fallback:** gradients flatten to `--grad-flat`.

## License
Brand assets © Newman. Code MIT.
