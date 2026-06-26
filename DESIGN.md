---
name: mosh.dog
description: Community link platform for the pup and furry underground
colors:
  bg: "#0a0a0a"
  surface: "#181620"
  surface-2: "#242030"
  ink: "#f0edf8"
  primary: "#c49338"
  primary-deep: "#6b4f1a"
  laser: "#b034cc"
  laser-deep: "#750a8a"
  accent: "#8c2020"
  accent-deep: "#5a1414"
  muted: "#86828c"
  border: "#28222e"
  success: "#4a9e56"
typography:
  display:
    fontFamily: "Outfit, system-ui, sans-serif"
    fontSize: "clamp(3rem, 8vw, 6rem)"
    fontWeight: 900
    lineHeight: 1
    letterSpacing: "-0.025em"
  headline:
    fontFamily: "Outfit, system-ui, sans-serif"
    fontSize: "clamp(1.75rem, 4vw, 2.75rem)"
    fontWeight: 800
    lineHeight: 1.1
    letterSpacing: "-0.02em"
  title:
    fontFamily: "Inter, system-ui, sans-serif"
    fontSize: "clamp(1.1rem, 2vw, 1.375rem)"
    fontWeight: 600
    lineHeight: 1.3
  body:
    fontFamily: "Inter, system-ui, sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.65
  label:
    fontFamily: "Inter, system-ui, sans-serif"
    fontSize: "0.75rem"
    fontWeight: 500
    lineHeight: 1.25
    letterSpacing: "0.05em"
rounded:
  none: "0"
  sm: "3px"
  md: "6px"
  lg: "12px"
  pill: "9999px"
spacing:
  xs: "4px"
  sm: "8px"
  md: "16px"
  lg: "24px"
  xl: "40px"
  2xl: "64px"
  3xl: "96px"
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.bg}"
    rounded: "{rounded.sm}"
    padding: "14px 32px"
  button-primary-hover:
    backgroundColor: "{colors.primary-deep}"
    textColor: "{colors.ink}"
  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.primary}"
    rounded: "{rounded.sm}"
    padding: "13px 31px"
  button-secondary-hover:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.primary}"
  link-card:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    rounded: "{rounded.sm}"
    padding: "16px 24px"
  link-card-hover:
    backgroundColor: "{colors.surface-2}"
    textColor: "{colors.ink}"
---

<!-- SEED: new design system, not yet implemented. Re-run /impeccable document once the first surface is built to capture real tokens and components. -->

# Design System: mosh.dog

## 1. Overview

**Creative North Star: "The Black Room"**

A black room where pups and furs dance under UV and green laser light, leather gear absorbing the dark, neon suits cutting the air, the bass punching through your chest. Two things are true at once: this is a leather community and a rave community, and the design holds both without choosing between them. The surface is pure void-black. The warmth of polished amber hardware glows against it. Above that, a single electric UV violet cuts through — not as decoration, but as a laser does: one clean line of light in the dark.

Typography is deliberate without being loud. Outfit Black at display scale is a geometric grotesque with character — clean and well-made, the kind of type you'd find on a quality leather goods catalog or a well-considered community brand. Not condensed-industrial, not literary serif. Just confident. Inter handles everything else: neutral, humanist, invisible. The pairing earns attention at the level that matters (the profile name, the heading) and disappears where it doesn't (labels, nav, form fields).

Motion is choreographed but fast. Entrances stagger. Sequences are deliberate. Nothing lingers past 250ms. The laser violet appears as glow — `box-shadow`, not fill — in high-concentration moments: avatar borders, active link cards, focus rings. The amber is the warm constant; the violet is the flash.

**Key Characteristics:**
- Void-black ground with cool violet-tinted surfaces (UV club wall, not leather bar wood)
- Amber (warm, leather) glows against cool dark surfaces — the tension is the point
- One laser accent: electric UV violet — used as glow and stroke, not as fill
- Outfit Black/ExtraBold as the display geometric with personality; Inter for all body and UI text
- Choreographed but fast motion at 120–250ms; laser glow animates on specific trigger moments
- WCAG 2.2 AA minimum throughout; the dark-first palette makes high contrast on-brand, not a trade-off

## 2. Colors: The Dark Room Palette

Three temperatures. Void-black ground. Warm amber leather. Cold UV laser violet. Each is specific; none bleeds into the others.

**The Three Lights Rule.** Three light sources, three colors. Amber: the warm bounce off leather hardware, the bar behind the DJ. Violet: the UV laser cutting through fog. Crimson: the exit sign, the danger state, the edge. No fourth light source. No additional accent colors.

### Primary
- **Amber / Polished Hardware** (`#c49338`, canonical `oklch(0.72 0.145 75)`): Leather warmth. Active navigation, icon fills, link underlines, avatar ring borders, primary button fills. Dark text (`bg`) on amber fills — contrast 9.5:1 (WCAG AAA). Amber is the constant warmth in a cold, dark room.
- **Dark Amber / Copper** (`#6b4f1a`, canonical `oklch(0.42 0.155 75)`): Hover and pressed state for amber fills.

### Secondary — Laser
- **Electric Violet / UV** (`#b034cc`, canonical `oklch(0.55 0.23 312)`): The UV blacklight. One laser accent, used exclusively as glow, stroke, and active-state signal. It never fills a background surface. It appears on avatar borders in special states, link-card active borders, focus rings on laser-coded elements, and sparse brand moments. At `L=0.55`, it reaches 3.8:1 contrast against `bg` — sufficient for large decorative text and icons, not for body copy. Always pair laser violet text with `font-size ≥ 1rem` and `font-weight ≥ 600`.
- **Dark Violet** (`#750a8a`, canonical `oklch(0.33 0.20 308)`): The deep-dark counterpart. Used only in tinted badge backgrounds and laser-deep glow shadow layers.

### Tertiary
- **Deep Crimson / Exit Sign** (`#8c2020`, canonical `oklch(0.45 0.180 22)`): Not a brand color — a function color. Destructive actions, reject buttons, danger states. The red exit sign in the dark room.
- **Dark Crimson** (`#5a1414`, canonical `oklch(0.30 0.170 22)`): Hover/pressed state for crimson fills.

### Neutral
- **Void Black** (`#0a0a0a`, canonical `oklch(0.06 0.000 0)`): The ground. No chroma — achromatic, absolute. The room with the lights off.
- **Club Surface** (`#181620`, canonical `oklch(0.12 0.005 290)`): Cards, panels, navigation backgrounds, input fields. A trace of cool violet — the UV ambient on a dark wall, not warmth, not haze. Barely perceptible, unmistakably intentional.
- **Elevated Club Surface** (`#242030`, canonical `oklch(0.17 0.008 290)`): Hover states for surface elements; slightly elevated panels; link-card hover backgrounds.
- **UV-Lit White** (`#f0edf8`, canonical `oklch(0.95 0.010 290)`): Near-white body text with a trace of violet-cool. Whites look this way under UV. Not warm, not neutral — the specific quality of white in a dark room with UV overhead.
- **Muted** (`#86828c`, canonical `oklch(0.55 0.010 290)`): Secondary text, placeholders, metadata. Cool-gray, shifted toward violet. Contrast ≈ 5.0:1 against `bg`.
- **Border** (`#28222e`, canonical `oklch(0.20 0.012 290)`): Dividers, card edges, input strokes. Cool-dark with trace violet.

### Semantic
- **Success Green** (`#4a9e56`, canonical `oklch(0.62 0.155 145)`): Approved states in the moderation queue only. Functional semantic, not brand.

### Named Rules
**The Void Surface Rule.** The body background is `#0a0a0a` — achromatic (`oklch(0.06 0.000 0)`), no chroma. The surface tokens carry the cool violet tint. Never put chroma in the bg; it breaks the depth stack.

**The Cold Room Rule.** All neutral surfaces tint toward cool violet (hue ~290), not warm amber. The amber `primary` glows AGAINST the cool ground — the tension between warm leather and cool UV is the system's defining character. Adding warmth to the surfaces dissolves the contrast that makes amber read as amber.

**The Laser as Glow Rule.** Electric violet (`laser`) never fills a card, panel, or button background. It appears exclusively as: (1) `box-shadow` glow layers, (2) border strokes on focused or active elements, (3) sparse text on large-scale brand moments where `font-size ≥ 1rem` and `font-weight ≥ 600`. "Laser" is a point of light, not a surface.

**The Dark Text on Amber Rule.** The amber primary at `oklch(0.72 0.145 75)` carries dark text (`bg`) — not white. Contrast is 9.5:1 (WCAG AAA). This is hardware labeling, not warning buttons. Don't override.

## 3. Typography: Geometric Display + Neutral Body

**Display Font:** Outfit (weights 800–900, via Google Fonts)
**Body Font:** Inter (weights 400–600, via Google Fonts or system-ui fallback)

**Character:** Outfit Black at display scale is confident and well-made — a geometric grotesque that reads as a deliberate choice rather than the default. Its proportions are clean and generous; the perfectly circular O, the double-storey lowercase g, the slightly distinctive R. It has personality without announcing it. At Black (900) it commands a profile name. At ExtraBold (800) it holds a page header without shouting. Inter complements it from a different axis: humanist where Outfit is geometric, neutral where Outfit has character. The pairing is quiet — the amber and violet do the identity work; the type gets out of the way unless it has something to say.

### Hierarchy
- **Display** (Outfit 900, `clamp(3rem, 8vw, 6rem)`, lh 1.0, ls -0.025em): Profile names at hero scale. Section titles on landing surfaces. `text-wrap: balance`.
- **Headline** (Outfit 800, `clamp(1.75rem, 4vw, 2.75rem)`, lh 1.1, ls -0.020em): Page headers, card titles, modal headings. `text-wrap: balance`.
- **Title** (Inter 600, `clamp(1.1rem, 2vw, 1.375rem)`, lh 1.3): Section subheadings, panel headers, navigation labels at desktop.
- **Body** (Inter 400, `1rem`, lh 1.65): All prose, form copy, link descriptions, bio text. Max line length 65ch.
- **Label** (Inter 500, `0.75rem`, lh 1.25, ls 0.05em, uppercase): Field labels, nav links, button text, chip text, status badges.

### Named Rules
**The Outfit Scale Rule.** Outfit appears only at Display and Headline scale — `clamp(1.75rem...)` and above. Below that threshold, Inter takes over. Outfit at small sizes loses the geometric clarity that earns its place.

**The Weight Floor Rule.** Outfit at weight 700 or below on dark backgrounds starts reading as a generic grotesque. Weights 800 and 900 only — the weight is the character.

## 4. Elevation

Dark-first system. Traditional box shadows are invisible on void-black surfaces. Depth comes from two sources: **tonal layering** (`surface` lifts above `bg`; `surface-2` lifts above `surface`) and **laser glow** (electric violet at low opacity signals state, not depth).

The violet glow is the system's most distinctive elevation material. It doesn't "lift" elements — it marks them as active, focused, or hovered. The physical reference is a laser cutting through floor haze and landing on something. Use it exactly that sparingly.

### Shadow Vocabulary
- **Amber Focus Glow** (`0 0 0 3px rgba(196, 147, 56, 0.22)`): Focus rings on amber-coded interactive elements (primary buttons, amber-bordered inputs).
- **Laser Focus Glow** (`0 0 0 3px rgba(176, 52, 204, 0.28)`): Focus rings on laser-coded elements; avatar halos in active states. The violet flash.
- **Avatar Halo** (`0 0 0 4px rgba(176, 52, 204, 0.16)`): Resting state for profile avatar border. Constant, dim violet ambient.
- **Avatar Halo Active** (`0 0 0 8px rgba(176, 52, 204, 0.35)`): Profile avatar on hover or in a featured position. The UV spotlight.
- **Panel Lift** (`0 1px 0 0 rgba(255, 255, 255, 0.04) inset`): Subtle inner-top highlight on raised surface components. Ambient bounce on a cool dark surface.

### Named Rules
**The Glow-Only Rule.** Box shadows with dark `rgba(0,0,0,...)` are invisible on void-black surfaces and prohibited. State is communicated with amber or violet glow, not shadow depth.

**The Violet Glow Budget.** At most two violet glows per viewport at any time. If three elements are all glowing violet simultaneously, none of them read as laser — they read as a purple UI. Laser is specific; specificity is the point.

## 5. Components

### Buttons
Square-edged (3px radius — almost sharp, not pill). Uppercase label in Inter 600. Never rounded-full.

- **Primary:** Amber fill (`primary`), dark `bg` text. 14px/32px padding. Hardware label read. Hover: `primary-deep` fill, text shifts to `ink`, translateY(-1px), 120ms ease-out-quart.
- **Focus:** Amber glow (`0 0 0 3px rgba(196,147,56,0.22)`).
- **Secondary / Ghost:** Transparent fill, `primary` amber border (1px) + text. Hover: `surface` fill.
- **Destructive:** Crimson fill (`accent`), `ink` text. Reject/delete only. Hover: `accent-deep`. Laser violet is not used in destructive states.

### Link Cards
Full-width rows — not SaaS cards. The core unit of every public profile.

- **Resting state:** `surface` (`#181620`) fill, 1px `border` edge, amber icon left-anchored, `muted` arrow right.
- **Hover:** `surface-2` fill, 1px `primary` amber border, arrow shifts to `primary`, translateX(3px).
- **Active/featured card:** 1px `laser` violet border, laser avatar halo on associated profile thumbnail if present. This is the only place the laser violet appears on a link card.
- **Padding:** 16px 20px. **Radius:** 3px.

### Inputs / Fields
- **Style:** `surface` fill, 1px `border` stroke, 3px radius.
- **Focus:** Amber border (`primary`), amber glow (`0 0 0 3px rgba(196,147,56,0.18)`). Amber, not violet — forms are a warm-amber interaction surface.
- **Placeholder:** `#504a58` (cool-violet dark gray; 4.5:1 against `surface`).
- **Labels:** Inter 500, 0.75rem, 0.05em tracking, uppercase, `muted`.

### Navigation
- **Background:** `surface` (`#181620`), 1px `border` bottom.
- **Brand mark:** Outfit 800, `primary` amber — the geometric identity marker in the cool dark surface.
- **Links:** Inter 500, 0.8125rem, 0.04em tracking, uppercase; `muted` at rest; `ink` on hover with `surface-2` bg; `primary` for active.

### Profile Header (Public Pages)
The UV spotlight moment — this is where the laser violet earns its most prominent use.

- **Avatar:** 88px circle, 2px `laser` violet border ring, dim laser halo (`0 0 0 6px rgba(176,52,204,0.18)`). On hover: halo expands (`0 0 0 12px rgba(176,52,204,0.32)`).
- **Name:** Outfit Black (Display scale), `ink`. The identity moment.
- **Bio:** Inter 400, `muted`, max-width 42ch, `text-wrap: pretty`.
- **Transition:** Avatar halo expansion 200ms ease-out-quart.

### Moderation Queue Row
Compact and functional. Amber approve, ghost reject that turns crimson on hover.

- **Row:** `surface` fill, 1px `border`.
- **Title:** Inter 600, `ink`. **URL:** `primary` amber (clickable). **From:** `muted`.
- **Approve:** Amber fill, dark text (primary button variant). **Reject:** Ghost — `muted`/`border` at rest; `accent` text + `accent` border on hover.

### Status Badges
- **Style:** 3px radius (not pill), Inter 500, uppercase, Label scale.
- **Pending:** Amber tint — `rgba(196,147,56,0.12)` bg, `primary` text, `rgba(196,147,56,0.30)` border.
- **Approved:** Success tint — `rgba(74,158,86,0.12)` bg, `#5db869` text, `rgba(74,158,86,0.30)` border.
- **Rejected:** Crimson tint — `rgba(140,32,32,0.15)` bg, `#c45050` text, `rgba(140,32,32,0.30)` border.

### Signature: Profile Avatar with UV Halo
The visual identity of a mosh.dog public profile page. A small circle in a UV glow — the laser landing on something. This component has the highest design concentration in the system; it should be visually perfect.

- 88–96px circle, `object-fit: cover`.
- 2px solid `laser` violet border.
- Resting: `0 0 0 6px rgba(176, 52, 204, 0.18)` outer glow.
- Hover: `0 0 0 12px rgba(176, 52, 204, 0.34)` — the UV spotlight expands.
- Transition: `box-shadow 200ms cubic-bezier(0.25, 1, 0.5, 1)`.
- The display name in Outfit Black below it — confident geometry under a UV spotlight.

## 6. Do's and Don'ts

### Do:
- **Do** keep `bg` as `#0a0a0a` — achromatic, no chroma. It's the void. The colors live above it.
- **Do** tint all neutral surfaces cool/violet (`hue ~290`), not warm. Amber glows AGAINST cool surfaces; warm surfaces dissolve the tension.
- **Do** use the laser violet exclusively as glow and stroke — never as a fill, never as a background surface.
- **Do** use Outfit at display and headline scale only (weights 800–900). Below that, switch to Inter.
- **Do** dark text (`bg`) on amber fills — 9.5:1 contrast, hardware labeling, intentional.
- **Do** keep violet glows to at most two per viewport simultaneously. Laser specificity = laser impact.
- **Do** cap motion durations at 250ms. Choreographed, never theatrical. The violet avatar halo expansion (200ms) is the longest allowed non-skeleton transition.
- **Do** `@media (prefers-reduced-motion: reduce)` on every animation.
- **Do** use OKLCH in prose as the canonical reference; hex in code.

### Don't:
- **Don't** use neon colors everywhere, or as background fills, or as gradients. This is not synthwave. The rule: one specific laser color (`laser` violet), one specific location (glow + stroke), no decorative bleed. Generic "rave neon aesthetic" is as much an anti-reference as generic "dark SaaS."
- **Don't** use gradient text (`background-clip: text` on a gradient). Single solid colors only. The laser violet as a text color must be solid, not gradient, and only at ≥1rem/600 weight.
- **Don't** use RGB gradients, purple-to-pink gradients, or multiple neon accent colors bleeding into each other. That's the synthwave trap. One laser hue, used precisely.
- **Don't** use Linktree, Beacons, or generic link-in-bio patterns: rounded-pill buttons, pastel fills, gradient rainbow backgrounds. Anti-reference by name.
- **Don't** use Hope UI, Bootstrap-default, or out-of-the-box admin skins. Replace them.
- **Don't** add glassmorphism (backdrop-filter: blur) as a default card treatment.
- **Don't** use side-stripe borders (`border-left` or `border-right` > 1px as a colored accent). Full borders, tinted backgrounds, or nothing.
- **Don't** use Outfit below 1.5rem or at weight 700 or below — it loses the geometric clarity that makes it worthwhile.
- **Don't** use box-shadow with dark `rgba()` on void-black surfaces — invisible. Use amber or violet glows instead.
- **Don't** add tracked all-caps eyebrows above every section. Label hierarchy is a system element, not a section scaffold.
- **Don't** let the violet glow appear on more than two elements in the same viewport. It stops reading as laser and starts reading as theme.
