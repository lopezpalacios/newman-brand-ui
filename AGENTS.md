# AGENTS.md

Operating manual for AI agents (and humans) working in this repo. Read this first.

## What this is
The **Newman brand guidelines** — a living styleguide (`index.html`) plus the design system
it documents. Static, dependency-free (HTML/CSS/JS), deployed to GitHub Pages via Actions.
**`index.html` is a styleguide, NOT a marketing landing page.** Keep it that way.

## Source of truth (in priority order)
1. `docs/DESIGN.md` — the design system spec (Google Stitch format). **Authoritative.**
2. `design-tokens.json` — machine-readable mirror of the tokens (W3C DTCG).
3. `assets/css/newman.css` `:root` — the runtime tokens. Must match 1 & 2.

If you change a token, change all three in the same commit, or you've introduced drift.

## Hard invariants (do not violate)
- **No chrome gradients.** The navy→magenta gradient exists ONLY inside the logo isotype
  SVG. Bars, buttons, rules, text, badges, stats = solid `--accent` (`#621558`).
- **Light, purple-forward, flat.** Canvas `--bg #F6F4F9`, text `--text #221A33`. No
  near-black surfaces. No drop shadows except modal/toast.
- **Logo on dark/colored = reversed all-white** lockup. The gradient isotype camouflages on
  any dark surface (navy footer, accent `#621558` nav pill). The nav pill is `--accent`.
- **Display headlines = Montserrat weight 300.** Never bold display.
- **Magenta only as the 4px label square.** Never magenta body text (use `--magenta-ink`).
- **Accessibility:** keep skip link, `:focus-visible` rings, ARIA on widgets,
  `prefers-reduced-motion`. Every text/bg pair must pass WCAG AA.
- **No build step, no runtime deps.** Plain HTML/CSS/JS. `index.html` stays at repo root
  (GitHub Pages serves from `/`).

## Layout
```
index.html              styleguide (root — Pages needs it)
assets/css/newman.css   tokens + components      assets/js/newman.js   behavior (IIFE → window.Newman)
assets/img/             logo SVG/PNG, og-image, icon-*    favicon.* · apple-touch-icon · site.webmanifest
docs/                   DESIGN.md (truth) · BRAND.md · brandbook.html
design-tokens.json      DTCG tokens     prompts/   reusable review prompts
.github/workflows/      pages.yml (deploy)
```

## Workflow
- Run locally: `npm start` → http://localhost:8000
- Visual check (macOS, no browser): `qlmanage -t -s 1400 -o /tmp index.html` then open the PNG.
- Format: `npm run format`. Commit style: Conventional Commits.
- Deploy: push to `main` → Actions builds Pages. Verify the run + that the URL returns 200.

## Known gaps / good next tasks
- `docs/brandbook.html` is the **old V1** (dark + gradient + lorem) and contradicts the v3
  system. Either reconcile it to v3 or relabel it as a V1 archive.
- OG image (`assets/img/og-image.jpg`) still uses a marketing line, not "Brand Guidelines".
- The `/newman-ui` Claude skill (`~/.claude/skills/newman-ui/`) must stay in sync with v3.
- No CI validation (format/lint/link-check/lighthouse) — only deploy.

## Related
The `/newman-ui` skill regenerates this system for new pages. The repo is its canonical
reference implementation; keep them in lockstep.
