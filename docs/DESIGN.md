---
version: alpha
name: Newman
description: >
  Newman · Soluciones en Energía. An energy platform financing and commercializing
  solar generation and behind-the-meter storage across Mexico and LATAM. Visual
  language: a restrained, near-monochrome navy/ink/paper canvas where a single
  navy→magenta gradient is the ~1% accent. Whisper-light Montserrat display type
  feels architectural; the 5-bar solar-ray isotype and a 4px square label indicator
  carry the brand. Flat and shadowless — hierarchy comes from tonal layering and
  generous spacing, never elevation.
colors:
  navy:        "#191B4D"
  magenta:     "#B80E65"
  magenta-ink: "#8A0A4B"
  indigo:      "#211A4E"
  plum:        "#3A1852"
  grape:       "#621558"
  berry:       "#981060"
  ink:         "#0A0A0C"
  onyx:        "#0F0E12"
  graphite:    "#3A3A42"
  grey:        "#74747F"
  cloud:       "#B9B9C2"
  line:        "#E7E7EA"
  paper:       "#F5F5F4"
  white:       "#FFFFFF"
  gradient:    "linear-gradient(105deg in oklch, #191B4D, #3A1852, #981060, #B80E65)"
typography:
  display:
    fontFamily: "Montserrat, 'Arial Narrow', Arial, sans-serif"
    fontSize: "64px"
    fontWeight: 300
    lineHeight: 1.02
    letterSpacing: "0.01em"
  heading:
    fontFamily: "Montserrat, sans-serif"
    fontSize: "32px"
    fontWeight: 500
    lineHeight: 1.15
    letterSpacing: "0.005em"
  subheading:
    fontFamily: "Montserrat, sans-serif"
    fontSize: "22px"
    fontWeight: 500
    lineHeight: 1.3
  body:
    fontFamily: "Inter, -apple-system, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.6
  body-sm:
    fontFamily: "Inter, sans-serif"
    fontSize: "14px"
    fontWeight: 400
    lineHeight: 1.4
  label:
    fontFamily: "Montserrat, sans-serif"
    fontSize: "12px"
    fontWeight: 400
    lineHeight: 1.3
    letterSpacing: "0.14em"
    fontFeature: "uppercase"
rounded:
  sm: "8px"
  nav: "16px"
  input: "12px"
  card: "24px"
  media: "64px"
  pill: "100px"
spacing:
  unit: 4
  4: "4px"
  8: "8px"
  12: "12px"
  16: "16px"
  24: "24px"
  36: "36px"
  48: "48px"
  60: "60px"
  96: "96px"
  120: "120px"
components:
  nav:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.white}"
    rounded: "{rounded.nav}"
    padding: "14px 24px"
  button-primary:
    backgroundColor: "{colors.gradient}"
    textColor: "{colors.white}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.pill}"
    padding: "14px 26px"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.navy}"
    rounded: "{rounded.pill}"
    padding: "14px 26px"
  card:
    backgroundColor: "{colors.white}"
    textColor: "{colors.graphite}"
    rounded: "{rounded.card}"
    padding: "{spacing.36}"
  section-label:
    textColor: "{colors.magenta-ink}"
    typography: "{typography.label}"
  media:
    rounded: "{rounded.media}"
  accordion-toggle:
    backgroundColor: "{colors.white}"
    textColor: "{colors.navy}"
    rounded: "{rounded.pill}"
    size: "40px"
  footer:
    backgroundColor: "{colors.onyx}"
    textColor: "{colors.cloud}"
---

## Overview

Newman should feel like a **technical specification rendered as a brand** — precise,
confident, bankable, and quietly optimistic about energy's future. The interface is
**near-colorless by design**: a warm-neutral paper canvas, ink/navy typography, and a
single navy→magenta gradient that appears only as a deliberate accent. Restraint is the
point — every element earns its place through **scale, spacing, and shape**, not hue.

The personality is **visionary, solid, bold, human** (brandbook voice). Bilingual EN/ES,
equally fluent. Lead with impact, back it with evidence; never hype, jargon, or
corporate-cold. When no specific rule applies, choose the more restrained, more
spacious, lower-chroma option — the absence of color is the design.

Target audience: EPC partners, project developers, and institutional capital. The work
is industrial (solar arrays, storage, factory floors) so the UI **softens** it with
generous rounding and whisper-light type rather than amplifying it with bold shouting.

## Colors

Two poles anchor everything — **Newman Navy** `#191B4D` and **Newman Magenta** `#B80E65`
— bridged by the signature gradient. Black/white/navy/paper form the high-contrast canvas
the brand lives on; magenta and the full gradient are the remaining ~1% accent.

| Token | Value | Role |
|-------|-------|------|
| `navy` | `#191B4D` | Primary. Gradient origin. Borders, headings on light, dark surfaces, the carbon tonal layer. |
| `magenta` | `#B80E65` | Accent only. Gradient apex, focus ring, the 4px label square. **Never** body text or large fills. |
| `magenta-ink` | `#8A0A4B` | The **only** magenta permitted as text on light — passes WCAG AA. Use for kickers/labels. |
| `indigo` `plum` `grape` `berry` | `#211A4E` `#3A1852` `#621558` `#981060` | Internal gradient stops. Not used as flat fills. |
| `ink` | `#0A0A0C` | Hero/nav-pill canvas, deepest interactive surface. |
| `onyx` | `#0F0E12` | Footer terminator — the only full-width dark surface. |
| `graphite` | `#3A3A42` | Body copy on light. |
| `grey` | `#74747F` | Muted/secondary text, captions, disabled. |
| `cloud` | `#B9B9C2` | Body copy on dark, hairline hover. |
| `line` | `#E7E7EA` | Hairline borders, dividers, card edges. |
| `paper` | `#F5F5F4` | **Page canvas** — the warm off-white that defines the surface. |
| `white` | `#FFFFFF` | Elevated cards, wells above the paper canvas. |

**Gradient:** `navy → magenta` only, never reversed, interpolated in **OKLCH** (sRGB
fallback) to kill the muddy plum mid-band. Reserve it for: the brand bar, one hero word,
the primary button, the isotype, the badge, and label squares. Nothing else.

## Typography

**Montserrat** carries all display/headline/label use; **Inter** handles body. The single
most distinctive choice is **weight 300 at display sizes** — the whisper-light headline
makes industrial copy read as *etched specification* rather than shout. Never set display
in 600/700. Open tracking `0.01em` keeps the light weight from feeling cramped.

| Role | Family | Size | Weight | Line | Tracking |
|------|--------|------|--------|------|----------|
| display | Montserrat | clamp(40–64px) | 300 | 1.02 | 0.01em |
| heading | Montserrat | 32px | 500 | 1.15 | 0.005em |
| subheading | Montserrat | 22px | 500 | 1.3 | — |
| body | Inter | 16px | 400 | 1.6 | — |
| body-sm | Inter | 14px | 400 | 1.4 | — |
| label | Montserrat | 12px | 400 | 1.3 | 0.14em, UPPERCASE |

Labels are uppercase, tracked, and **prefixed by a 4–6px solid magenta square** — never a
bullet, dot, icon, or emoji. Body stays sentence case with default tracking. Never
Montserrat below 12px; never tint body text magenta.

## Layout

Max-width **1200px** centered; hero breaks full-bleed. **4px base unit**; the `spacing`
scale drives all rhythm, with **~48px section gaps** and comfortable internal density.
Content alternates single-column editorial stacks and two-column text/media splits —
**deliberately asymmetric**, left-aligned by default. Avoid centering everything; reserve
centered blocks for short statements only. Navigation is a **floating dark pill** anchored
top, not a full-width bar. No sidebar, no mega-menu, no sticky beyond the nav.

## Elevation & Depth

**Deliberately shadowless.** All hierarchy is tonal layering —
`paper → white → navy(carbon) → onyx` — plus generous spacing, never drop shadows. This
keeps the interface flat, precise, and instrument-like. The only exceptions are transient
overlays (modal, toast), which may carry a single soft shadow to lift off the page.

## Shapes

Generous, pill-and-orb rounding is a signature: **buttons/pills `100px`**, **image
portholes `64px`**, **cards `24px`**, **nav `16px`**, **inputs `12px`**. Nothing drops
below `8px` — sharp corners read as foreign here. The 5-bar isotype's diagonal geometry
is the one angular motif; everything else is soft.

## Components

- **Nav pill** — ink `#0A0A0C`, 16px radius, floats over paper; white links at 14px,
  contrast alone separates it (no shadow). Isotype on the left.
- **Primary button** — gradient fill, white 14px, 100px pill, no border/shadow. Highest
  interactive weight; use sparingly (one per view).
- **Ghost button** — transparent, 1.5px navy border, navy text, same 100px geometry — a
  matched pair to the primary.
- **Section label** — 4–6px solid magenta square + uppercase tracked `magenta-ink` text.
- **Display headline** — Montserrat 300, clamp 40–64px, line-height ~1.0; optionally one
  word in gradient text.
- **Card** — white surface, `line` hairline, 24px radius, 36px padding, flat (border
  darkens on hover, no shadow).
- **Media porthole** — full-bleed, 64px radius, no frame/scrim/caption-box.
- **Accordion** — hairline rows; right-aligned 40px circular toggle (navy border, white
  fill, `+`/`−`).
- **Footer** — onyx `#0F0E12`, gradient-bar cap, the page's definitive terminator.

## Do's and Don'ts

**Do**
- Lead with paper/white/navy for ~99% of any surface; let the gradient be the rare accent.
- Set display headlines in Montserrat **300** at large sizes with ~1.0 line-height.
- Prefix every section label with the 4px solid magenta square.
- Keep rounding generous — 100px pills, 64px media, 24px cards.
- Build hierarchy from tonal layers + spacing; stay flat and shadowless.
- Use real industrial photography full-bleed at 64px radius when available.

**Don't**
- Don't run the gradient under body text, reverse it, add hues, or posterize it.
- Don't tint body text magenta — use `magenta-ink` for the small label accents only.
- Don't use bold/semibold for display headlines — the whisper-weight is the whole point.
- Don't add drop shadows to cards, buttons, or nav — flat tonal layering only.
- Don't add icons or emoji to labels — the square and typography carry all signaling.
- Don't center every block or ship three identical cards in a row — vary the rhythm.
- Don't ship gradient/solid color blocks as stand-in "images" — use real media or an
  intentional treatment, never an obvious placeholder.
