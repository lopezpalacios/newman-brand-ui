# Level-Up Review Prompt

A reusable prompt to push the Newman guidelines/system from "competent" to "distinctive +
production-grade + agent-ready". Broader than `devibe-review.md` (which only kills AI tells).
Anchored to `../docs/DESIGN.md` and `../AGENTS.md`.

> Paste into an agent with the repo open. It audits, scores, plans, then (on request) applies.

---

## Prompt

```
You are a principal design engineer reviewing the Newman brand-guidelines repo. Treat
docs/DESIGN.md as the spec and AGENTS.md as the invariants. Do NOT break any hard invariant.
Score each axis 1–5 with evidence (file:selector), then produce a ranked, surgical plan.

AXIS 1 — Distinctiveness (is it a brand, or a tasteful template?)
  □ Does anything beyond color say "Newman"? (type personality, the isotype as a hero
    moment, an ownable layout device — not just one accent on lilac)
  □ Is Montserrat a deliberate choice or the default geometric sans? If default, propose a
    more characterful grotesque (Space Grotesk, Geist, Söhne) OR justify keeping it.
  □ Is there rhythm variation between sections, or the same wrap→kicker→h-lg→rule→grid loop?
  □ Is there a real focal anchor above the fold (large isotype / asymmetry / scale jump)?

AXIS 2 — System completeness (is it actually a design system?)
  □ Component STATES shown: default/hover/focus/active/disabled/loading/error/empty?
  □ Is there a dark-theme token set, or only light?
  □ Semantic colors (success/warning/error/info) tuned to the brand, not raw red/green?
  □ Are tokens consistent across css :root ↔ design-tokens.json ↔ DESIGN.md (no drift)?
  □ Is brandbook.html coherent with the live v3 system, or a contradicting V1 artifact?

AXIS 3 — Accessibility (prove it, don't claim it)
  □ Run/representative-check contrast for ALL pairs incl. placeholder, disabled, on-accent,
    on-navy, focus ring. Report ratios.
  □ Keyboard: tab order, skip link target, focus visible everywhere, modal trap, tab roving.
  □ Reduced-motion honored; prefers-color-scheme respected if dark tokens exist.
  □ Semantics: landmarks, heading order, alt/aria-label on every SVG/control.

AXIS 4 — Performance & polish
  □ Fonts: is the Google Fonts request weight-trimmed / preloaded / swap? Self-host option?
  □ Any layout shift (CLS) from fonts/images? Image dims set?
  □ CSS unused-rule bloat; JS guards; no console errors.
  □ Favicon/OG/manifest correct and on-message (OG must not be a marketing line on a
    guidelines site).

AXIS 5 — Agent-readiness & DX
  □ AGENTS.md present, accurate, lists invariants + gaps?
  □ design-tokens.json present and in sync?
  □ CI VALIDATES (format check, htmlhint, link-check, lighthouse budget) — not just deploys?
  □ Is the /newman-ui skill in sync with the current system version?

OUTPUT:
  1) Scorecard (axis → /5 → one-line evidence).
  2) Ranked plan: P0 correctness/drift, P1 agent-ready/system gaps, P2 distinctiveness/polish.
     Each item: what, why, which DESIGN.md/AGENTS.md rule it serves, rough effort.
  3) On "apply P0/P1": make the changes, keep css ↔ tokens ↔ DESIGN.md in lockstep, run the
     qlmanage render to verify, and report before/after.
```

---

## Newman guardrails (never trade away for polish)
No chrome gradients (logo isotype only) · light flat surfaces · Montserrat 300 display ·
reversed white logo on dark · magenta only the label square · WCAG AA min · no build step.
