# Iconic Loop — Critique Log

Running record of the `prompts/iconic-loop.md` loop. One legendary-designer persona per
iteration → one critique → one shipped improvement → self-score.

**Persona rotation:** Paul Rand → Rob Janoff → **Saul Bass (next)** → Massimo Vignelli →
Paula Scher → Dieter Rams → Walter Landor → Michael Bierut → Stefan Sagmeister → Lindon Leader → (repeat).

**Iconicity axes (/10):** Reductive · Memorable · Scalable · Mono+Inverted · Distinct ·
Cross-cultural · Timeless · Systematic · Flexible.

---

## Iteration 1 — Paul Rand
**Doctrine:** "Don't try to be original, try to be good. A logo derives meaning from quality,
not the other way round. Reduce — and prove the system."

**Critique:** The mark had no published construction; iconic marks (Apple, FedEx) ship a grid
so the form is *reproducible, not drawn*. Monochrome/inverted survival and small-scale
legibility were claimed but never shown — unproven equity. The bigger open question: does the
silhouette read as an **N**, or merely as "dynamic stripes"? That's the memorability gap.

**Shipped:** Added a **Construction & tests** block to the Logo section — the isotype on a
10×10 unit grid with the shared ~42° diagonal axis drawn; a monochrome/inverted row (accent,
navy, white-on-black, black-on-white); and a 16→48px scale ladder. Reusable `<symbol id=nm-iso>`
+ `currentColor` so every tint is one source. Verified by isolated render.

**Self-score:** Reductive 8 · Memorable 6 · Scalable 9 · Mono+Inverted 9 · Distinct 6 ·
Cross-cultural 9 · Timeless 7 · Systematic 9 · Flexible 8.  **Avg ≈ 7.9.**
**Rand's verdict:** "Construction is honest now. Next, the *idea* must be unmistakable —
sharpen what the mark *says*. Memorability + distinctiveness are the work ahead."

**Next (Rob Janoff):** does it read in a single glance? Is the silhouette ownable and warm,
or generic? Pressure-test recognition.

---

## Iteration 2 — Rob Janoff
**Doctrine:** "It's recognizable, simple, and it works at any size. People should get it in a
glance — and the silhouette should own its space."

**Critique:** Equity was all in the horizontal lockup; the isotype had no defined life as a
standalone glyph — exactly where Apple's mark is strongest (the tile on a home screen). Without
an app-mark spec, the brand has no recognized at-a-glance form, and the dual meaning (N / rays)
was never stated for the reader.

**Shipped:** A **Recognition & app-mark** block — the reversed white isotype in a rounded
square (radius ≈25% w) across accent / navy / black tiles, plus a one-glance reading note (the
abstract **N** + solar **rays** dual meaning) and a cover-the-wordmark recognition test. New
`.app-tile` component. Verified by isolated render.

**Self-score:** Reductive 8 · Memorable 7 · Scalable 9 · Mono+Inverted 9 · Distinct 7 ·
Cross-cultural 9 · Timeless 7 · Systematic 9 · Flexible 9.  **Avg ≈ 8.2.**
**Janoff's verdict:** "Now it owns a tile and reads instantly. The diagonal energy is good —
next, make the *motion/idea* unmistakable so no one mistakes it for generic stripes."

**Next (Saul Bass):** reduce to the boldest possible symbol; is there one unforgettable gesture?
Could the mark imply motion/upward momentum even more decisively?
