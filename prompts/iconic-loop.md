# Iconic Loop — make the Newman mark & guidelines unbeatable

Goal: iterate the Newman logo + brand guidelines until a committee of legendary identity
designers is unanimously impressed and the mark passes the "iconic" test the way
Apple / Marlboro / Pepsi do — instantly recognized, culture-independent, timeless.

## The committee (rotate one persona per iteration, in order, then loop)
1. **Paul Rand** — the *idea* first; reduce to the essential; timelessness (IBM, NeXT, ABC).
2. **Rob Janoff** — recognition + warmth; the silhouette that reads in a glance (Apple).
3. **Saul Bass** — bold reductive symbol; motion; one shape you can't forget (AT&T, United).
4. **Massimo Vignelli** — grid, geometry, discipline; "the life of a designer is a life of fight against ugliness."
5. **Paula Scher** — typographic identity, scale, energy, ownable wordmark.
6. **Dieter Rams** — less, but better; honesty; will it look right in 20 years?
7. **Walter Landor** — consumer recognition; the chevron that built Marlboro; consistency.
8. **Michael Bierut** — system coherence across every application.
9. **Stefan Sagmeister** — emotional impact; does it move anyone?
10. **Lindon Leader** — the FedEx-arrow lesson: hidden ingenuity, negative space, "simple, memorable".

## Iconicity rubric (score each /10; mark must pass ALL to be "unbeatable")
- **Reductive** — works as a pure one-color silhouette.
- **Memorable** — redrawable from memory after 5 seconds.
- **Scalable** — crisp from 16px favicon to a billboard.
- **Monochrome + inverted** — survives black-on-white, white-on-black, single ink.
- **Distinct** — not confusable with competitors (solar/energy brands, other "N" marks).
- **Cross-cultural** — no language dependence, no culturally-loaded symbol.
- **Timeless** — not tied to a 2020s trend.
- **Systematic** — geometric construction can be reproduced on a grid.
- **Flexible** — one mark, many applications, one voice.

## Per-iteration procedure (each loop wake-up)
1. Read `docs/CRITIQUE-LOG.md`. Find the next persona and the current scorecard.
2. Adopt that persona. Critique the logo + guidelines in their doctrine — be specific and
   honest (no flattery). Name the single highest-leverage improvement.
3. Implement exactly **one** focused improvement. Honor the system invariants in `AGENTS.md`
   (no chrome gradients, accent `#621558`, light/flat, Montserrat 300, a11y) UNLESS the
   improvement is a deliberate, argued refinement of the mark itself — if so, document why.
4. Verify visually: `qlmanage -t -s 1200 -o /tmp index.html` (and render any new logo SVG).
   Keep css ↔ design-tokens.json ↔ DESIGN.md in lockstep.
5. Commit (Conventional Commits, persona in the body), push; confirm CI **Validate → Deploy**
   both green and the URL returns 200.
6. Append an entry to `docs/CRITIQUE-LOG.md`: persona, critique, change shipped, new self-score.
7. After every full pass of the committee (10 personas), write a **Committee Scorecard** row:
   each axis averaged, plus one-line consensus.

## Stop condition
Stop the loop when the committee scorecard reaches **≥ 9/10 on every axis** with a written
unanimous "this is iconic" consensus — OR the user says stop. On stop, push a one-line
summary via PushNotification.

## Guardrails
- The 5-bar solar-ray isotype is the brand's basis — refine, grid, and strengthen it; do not
  swap it for an unrelated mark without an explicit, recorded rationale.
- Every change must deploy green. Never leave Pages broken.
- One improvement per iteration — accumulate, don't churn.
