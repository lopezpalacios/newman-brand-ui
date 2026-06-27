---
version: alpha
name: Newman
description: >
  Newman · Soluciones en Energía. An energy platform financing and commercializing
  solar generation and behind-the-meter storage across Mexico and LATAM. Visual
  language (v3): a light, warm-lilac canvas with deep-aubergine text and ONE solid
  brand purple (#621558) as accent (also the floating nav pill) — no chrome gradients.
  Navy carries headlines and the footer anchor. The navy→magenta gradient survives ONLY
  inside the logo isotype (the registered mark). Whisper-light Space Grotesk display type
  feels architectural; the 5-bar isotype and a 4px magenta square label carry the
  brand. Flat and shadowless — hierarchy from tonal layering and spacing, never elevation.
colors:
  bg:          "#F6F4F9"   # page canvas — warm lilac-white
  bg-2:        "#ECE7F3"   # tinted panel / band
  surface:     "#FFFFFF"   # cards, wells
  accent-tint: "#F1E9F4"   # hover/selected surface
  text:        "#221A33"   # primary text — deep aubergine (15:1 on bg)
  muted:       "#5F5870"   # secondary text (6.1:1)
  navy:        "#191B4D"   # headlines + footer anchor
  accent:      "#621558"   # THE purple — buttons/links/rules/stats
  accent-hover:"#4C1043"
  magenta:     "#B80E65"   # highlight only — the 4px label square
  magenta-ink: "#8A0A4B"   # contrast-safe magenta text, if ever needed
  line:        "#E4DEF1"   # hairlines / borders
  white:       "#FFFFFF"
  on-dark:     "#EDEAF4"   # text on navy surfaces
  logo-gradient: "linear-gradient(105deg, #191B4D, #3A1852, #981060, #B80E65)"  # SVG isotype ONLY
typography:
  display:
    fontFamily: "Space Grotesk, 'Arial Narrow', Arial, sans-serif"
    fontSize: "64px"
    fontWeight: 300
    lineHeight: 1.02
    letterSpacing: "0.01em"
  heading:
    fontFamily: "Space Grotesk, sans-serif"
    fontSize: "32px"
    fontWeight: 500
    lineHeight: 1.15
    letterSpacing: "0.005em"
  subheading:
    fontFamily: "Space Grotesk, sans-serif"
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
    fontFamily: "Space Grotesk, sans-serif"
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
    backgroundColor: "{colors.accent}"
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
**light and low-chroma by design**: a warm-lilac canvas, deep-aubergine/navy typography,
and a single solid brand purple (`#621558`) as the deliberate accent — **no chrome
gradients**. Restraint is the point — every element earns its place through **scale,
spacing, and shape**, not hue.

The personality is **visionary, solid, bold, human** (brandbook voice). Bilingual EN/ES,
equally fluent. Lead with impact, back it with evidence; never hype, jargon, or
corporate-cold. When no specific rule applies, choose the more restrained, more
spacious, lower-chroma option — the absence of color is the design.

Target audience: EPC partners, project developers, and institutional capital. The work
is industrial (solar arrays, storage, factory floors) so the UI **softens** it with
generous rounding and whisper-light type rather than amplifying it with bold shouting.

## Colors

A light, purple-forward, **flat** system (v3). The canvas is warm lilac; text is deep
aubergine; one solid brand purple (`#621558`) does all accent work. Navy anchors headlines
and the single dark surface. All pairs pass WCAG AA (most AAA).

| Token | Value | Role | Contrast |
|-------|-------|------|----------|
| `bg` | `#F6F4F9` | **Page canvas** — warm lilac-white | — |
| `bg-2` | `#ECE7F3` | Tinted panel / band (replaces old dark slabs) | — |
| `surface` | `#FFFFFF` | Elevated cards, wells | — |
| `accent-tint` | `#F1E9F4` | Hover/selected surface | — |
| `text` | `#221A33` | Primary text — deep aubergine | 15:1 on bg |
| `muted` | `#5F5870` | Secondary text | 6.1:1 |
| `navy` | `#191B4D` | Headlines + footer (dark anchor) | 14.6:1 head |
| `accent` | `#621558` | **The** purple — nav pill, buttons/links/rules/stats | white-on 11.9:1 |
| `accent-hover` | `#4C1043` | Button hover | 14.4:1 |
| `magenta` | `#B80E65` | Highlight only — the 4px label square (graphic) | 5.8:1 |
| `magenta-ink` | `#8A0A4B` | Contrast-safe magenta text, if ever needed | 8.6:1 |
| `line` | `#E4DEF1` | Hairline borders, dividers, card edges | — |
| `on-dark` | `#EDEAF4` | Text on navy surfaces | — |

**Gradient policy:** there are **no UI/chrome gradients**. The navy→magenta gradient lives
**only inside the logo isotype** (the registered mark, in SVG). Accent fills, bars, rules,
stats, and the hero word are all the **solid** `accent`. This is deliberate — flat solid
color reads as designed; gradient chrome reads as vibe-coded.

## Typography

**Space Grotesk** carries all display/headline/label use; **Inter** handles body. The single
most distinctive choice is **weight 300 at display sizes** — the whisper-light headline
makes industrial copy read as *etched specification* rather than shout. Never set display
in 600/700. Open tracking `0.01em` keeps the light weight from feeling cramped.

| Role | Family | Size | Weight | Line | Tracking |
|------|--------|------|--------|------|----------|
| display | Space Grotesk | clamp(40–64px) | 300 | 1.02 | 0.01em |
| heading | Space Grotesk | 32px | 500 | 1.15 | 0.005em |
| subheading | Space Grotesk | 22px | 500 | 1.3 | — |
| body | Inter | 16px | 400 | 1.6 | — |
| body-sm | Inter | 14px | 400 | 1.4 | — |
| label | Space Grotesk | 12px | 400 | 1.3 | 0.14em, UPPERCASE |

Labels are uppercase, tracked, and **prefixed by a 4–6px solid magenta square** — never a
bullet, dot, icon, or emoji. Body stays sentence case with default tracking. Never
Space Grotesk below 12px; never tint body text magenta.

## Layout

Max-width **1200px** centered; hero breaks full-bleed. **4px base unit**; the `spacing`
scale drives all rhythm, with **~48px section gaps** and comfortable internal density.
Content alternates single-column editorial stacks and two-column text/media splits —
**deliberately asymmetric**, left-aligned by default. Avoid centering everything; reserve
centered blocks for short statements only. Navigation is a **floating dark pill** anchored
top, not a full-width bar. No sidebar, no mega-menu, no sticky beyond the nav.

## Elevation & Depth

**Deliberately shadowless.** All hierarchy is tonal layering —
`bg → bg-2 → surface(white) → navy` — plus generous spacing, never drop shadows. This
keeps the interface flat, precise, and instrument-like. The only exceptions are transient
overlays (modal, toast), which may carry a single soft shadow to lift off the page.

## Shapes

Generous, pill-and-orb rounding is a signature: **buttons/pills `100px`**, **image
portholes `64px`**, **cards `24px`**, **nav `16px`**, **inputs `12px`**. Nothing drops
below `8px` — sharp corners read as foreign here. The 5-bar isotype's diagonal geometry
is the one angular motif; everything else is soft.

## Components

- **Nav pill** — accent `#621558`, 16px radius, floats over the lilac canvas; reversed
  all-white logo + white links; CTA is a white pill with accent text. White-on-accent =
  11.9:1; contrast alone separates it (no shadow).
- **Primary button** — solid `accent` fill, white 14px, 100px pill; hover → `accent-hover`.
  Highest interactive weight; use sparingly (one per view).
- **Ghost button** — transparent, 1.5px `accent` border, `accent` text, same 100px geometry
  — a matched pair to the primary (fills `accent` on hover).
- **Section label** — 4–6px solid `magenta` square + uppercase tracked `accent` text.
- **Display headline** — Space Grotesk 300, clamp 40–64px, line-height ~1.0, color `navy`;
  optionally one word in solid `accent`.
- **Card** — white surface, `line` hairline, 24px radius, 36px padding, flat (border →
  `accent` on hover, no shadow).
- **Media porthole** — full-bleed, 64px radius, no frame/scrim/caption-box.
- **Accordion** — hairline rows; right-aligned 40px circular toggle (`accent` border, white
  fill, `+`/`−`).
- **Footer** — navy `#191B4D`, solid `accent` bar cap, the page's definitive terminator.

## Do's and Don'ts

**Do**
- Lead with bg/surface/navy for ~99% of any surface; let solid `accent` be the rare highlight.
- Set display headlines in Space Grotesk **300** at large sizes with ~1.0 line-height.
- Prefix every section label with the 4px solid magenta square.
- Keep rounding generous — 100px pills, 64px media, 24px cards.
- Build hierarchy from tonal layers + spacing; stay flat and shadowless.
- Use real industrial photography full-bleed at 64px radius when available.

**Don't**
- Don't add chrome gradients — the gradient belongs only inside the logo isotype.
- Don't tint body text magenta — use `magenta-ink` for the small label accents only.
- Don't use bold/semibold for display headlines — the whisper-weight is the whole point.
- Don't add drop shadows to cards, buttons, or nav — flat tonal layering only.
- Don't add icons or emoji to labels — the square and typography carry all signaling.
- Don't center every block or ship three identical cards in a row — vary the rhythm.
- Don't ship gradient/solid color blocks as stand-in "images" — use real media or an
  intentional treatment, never an obvious placeholder.
