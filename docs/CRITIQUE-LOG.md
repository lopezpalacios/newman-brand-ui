# Iconic Loop — Critique Log

Running record of the `prompts/iconic-loop.md` loop. One legendary-designer persona per
iteration → one critique → one shipped improvement → self-score.

**Persona rotation:** Paul Rand → Rob Janoff → Saul Bass → Massimo Vignelli →
**Paula Scher (next)** → Dieter Rams → Walter Landor → Michael Bierut → Stefan Sagmeister → Lindon Leader → (repeat).

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

---

## Iteration 3 — Saul Bass
**Doctrine:** "Symbolize and summarize. A logo is identity in motion — make one gesture
unforgettable." (Bass invented the animated corporate identity: AT&T, United, Bell.)

**Critique:** A static mark stops at the page; Bass-era brands defined how the symbol *moves*.
Newman's diagonal bars beg for motion — they already imply descent/momentum — but the system
had no canonical animation, so every implementer would invent their own and dilute the gesture.

**Shipped:** A **Logo in motion** spec — the five bars rise and assemble in sequence (longest
first, ~0.6s, 90ms stagger, ease-out) as the signature splash/intro/loading gesture; build-only,
never disassemble; `prefers-reduced-motion` shows the formed mark. New `.logo-motion` component.

**Self-score:** Reductive 8 · Memorable 8 · Scalable 9 · Mono+Inverted 9 · Distinct 8 ·
Cross-cultural 9 · Timeless 7 · Systematic 9 · Flexible 9.  **Avg ≈ 8.4.**
**Bass's verdict:** "The gesture is right — energy coming online. Lock the timing as law so it's
the same everywhere. Timelessness is the last 10%: nothing here should feel of-the-moment."

**Next (Massimo Vignelli):** is the geometry truly disciplined? Grid, proportion, the wordmark's
type — is it Helvetica-grade timeless, or are there arbitrary decisions to remove?

---

## Iteration 4 — Massimo Vignelli
**Doctrine:** "The grid is the underwear of the book. Discipline. A handful of timeless
typefaces. If you can design one thing, you can design everything — through the system."

**Critique:** The page had a max-width but **no published grid** — the single most Vignelli
omission. A guidelines doc that doesn't show its own grid asks implementers to place by eye,
which guarantees drift. The type system was shown as specimens but never stated as a *limited
canon* (how many families, how many weights, what measure).

**Shipped:** A **Grid & measure** block — a visible 12-column grid (1200px, 24px gutters) plus
the stated discipline: two typefaces, four weights, one body measure (≤64ch), nothing placed by
eye. New `.grid-cols` component.

**Self-score:** Reductive 8 · Memorable 8 · Scalable 9 · Mono+Inverted 9 · Distinct 8 ·
Cross-cultural 9 · Timeless 8 · Systematic 10 · Flexible 9.  **Avg ≈ 8.7.**
**Vignelli's verdict:** "Now it has underwear. Systematic is excellent. The one arbitrary thing
left is the display typeface — Montserrat is competent but not timeless. That is the open
decision (flagged for the client). Everything else is disciplined."

**Next (Paula Scher):** is the wordmark doing enough? Type as image — could the identity be
bolder, more typographically expressive, more ownable at environmental scale?
