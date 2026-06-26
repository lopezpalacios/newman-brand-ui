# De-Vibe Review Prompt

A reusable prompt for auditing a frontend that "looks AI-generated / vibe-coded" and
turning it into something that reads as intentionally designed. Anchored to
[`../docs/DESIGN.md`](../docs/DESIGN.md).

> Paste the prompt below into an agent with the repo open. Replace `{TARGET}` with the
> page/component under review (e.g. `index.html`).

---

## Prompt

```
You are a senior product designer + front-end engineer doing a "de-vibe" review of {TARGET}.
The goal: remove every signal that the UI was machine-generated and make each choice read as
deliberate. Treat docs/DESIGN.md as the single source of truth — every fix must conform to it.

STEP 1 — Audit against the "vibe-coded tells" checklist. For each, mark PASS / FAIL / N/A with
one line of evidence (selector or screenshot region):

  Layout & rhythm
  □ Everything centered / one column / equal weight — no asymmetry or focal hierarchy
  □ Three identical cards in a row (or any uniform NxN grid as the default content shape)
  □ Mathematically even spacing everywhere; no intentional rhythm, no breathing asymmetry
  □ Generic hero: centered headline + subtext + two buttons (primary + ghost), nothing else

  Color & surface
  □ Default purple/indigo/blue gradient as the hero background
  □ Gradient or solid color BLOCKS standing in for real images ("forgot the photos")
  □ Drop shadows everywhere (shadow-md/lg) doing the hierarchy work
  □ Untouched framework palette (Tailwind slate/zinc, Bootstrap blue)

  Type
  □ One system/Inter font at default weights; no display personality or weight contrast
  □ Headlines all 600/700 bold; no light or oversized "architectural" option
  □ Default sizes/line-heights; no real type scale; tracking never touched

  Detail & content
  □ Emoji or stock icon bullets standing in for a considered indicator
  □ Lorem / vague filler copy left in a "finished" view
  □ Over-animation: every element fades/slides up on scroll
  □ Default radii (rounded-lg) on everything; no committed shape language
  □ No empty/loading/error states; no focus-visible; motion not reduced-motion aware

STEP 2 — Prioritize. Rank FAILs by visual impact (the image-placeholder and centered-everything
tells dominate first impressions). Note which are brand-locked vs free to change.

STEP 3 — Propose fixes as a diff plan, each citing the DESIGN.md rule it satisfies. Prefer:
  - Real or intentionally-treated media over color blocks (never an obvious placeholder).
  - Asymmetric, left-aligned editorial layout; vary content shapes (lists, splits, offsets).
  - A committed type system: one light/architectural display weight + real scale + tracking.
  - Flat tonal layering over shadows; restrained accent color (the brand's ~1%).
  - A considered indicator (here: the 4px square) instead of emoji/icons.
  - Staggered, restrained motion; full a11y (landmarks, ARIA, focus, reduced-motion).

STEP 4 — Apply the fixes, keeping the build dependency-free and DESIGN.md in sync. Re-run the
checklist; report before/after PASS counts and anything intentionally left (with rationale).

Output: (1) the audit table, (2) the ranked fix plan, (3) the applied diff summary,
(4) residual items + why.
```

---

## Newman-specific guardrails
- Gradient is the **~1% accent** — never hero-wide background, never under body text, never reversed.
- Magenta text only via `--magenta-ink`; display headlines stay **weight 300**.
- Keep it **flat/shadowless**; rounding stays generous (pills 100px, media 64px, cards 24px).
- Replace placeholder media with the **navy blueprint** treatment or real industrial photography —
  never a bare gradient/solid block.
