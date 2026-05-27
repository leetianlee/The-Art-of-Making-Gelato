---
name: The Art of Making Gelato
description: A quiet, precise recipe app for making gelato at home
colors:
  ink: "oklch(0.255 0.022 54)"
  ink-secondary: "oklch(0.440 0.028 52)"
  ink-muted: "oklch(0.548 0.026 56)"
  cream-bg: "oklch(0.984 0.008 74)"
  surface: "oklch(0.997 0.004 80)"
  warm-fill: "oklch(0.962 0.011 73)"
  hairline: "oklch(0.908 0.013 74)"
  divider: "oklch(0.855 0.018 72)"
  terracotta: "oklch(0.585 0.118 48)"
  terracotta-deep: "oklch(0.515 0.122 46)"
  terracotta-ink: "oklch(0.500 0.118 46)"
  terracotta-tint: "oklch(0.951 0.030 64)"
  terracotta-line: "oklch(0.882 0.045 58)"
  success: "oklch(0.515 0.090 152)"
  qa-amber: "oklch(0.498 0.072 70)"
typography:
  display:
    fontFamily: "Fraunces, Georgia, 'Times New Roman', serif"
    fontSize: "19px"
    fontWeight: 500
    lineHeight: 1.1
    letterSpacing: "-0.01em"
    fontFeature: "opsz auto"
  title:
    fontFamily: "Fraunces, Georgia, serif"
    fontSize: "17px"
    fontWeight: 500
    lineHeight: 1.2
    letterSpacing: "-0.01em"
  body:
    fontFamily: "-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif"
    fontSize: "15px"
    fontWeight: 400
    lineHeight: 1.55
  label:
    fontFamily: "-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif"
    fontSize: "10px"
    fontWeight: 600
    letterSpacing: "0.1em"
rounded:
  sm: "11px"
  md: "16px"
  pill: "999px"
spacing:
  xs: "4px"
  sm: "8px"
  md: "12px"
  lg: "16px"
components:
  pill-filter:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink-secondary}"
    rounded: "{rounded.pill}"
    padding: "8px 15px"
  pill-filter-active:
    backgroundColor: "{colors.terracotta}"
    textColor: "{colors.surface}"
    rounded: "{rounded.pill}"
    padding: "8px 15px"
  copy-button:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.terracotta-ink}"
    rounded: "{rounded.sm}"
    padding: "10px 15px"
  recipe-card:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.md}"
    padding: "15px 16px"
  search-input:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    rounded: "12px"
    padding: "11px 14px"
---

# Design System: The Art of Making Gelato

## 1. Overview

**Creative North Star: "The Quiet Gelateria"**

The interface behaves like a good gelato counter: warm, unhurried, and confident enough to let the product speak. It is read at arm's length, on a phone propped on the kitchen counter, by someone whose hands are busy and whose attention is split. So the work is to recede. Cream surfaces and a single terracotta accent carry the whole system; the recipes are the content and the chrome stays out of the way. It is a tool first, but it is also a thing the owner is proud of, so the craft shows in precision rather than ornament: exact spacing, aligned figures, a single optical serif used sparingly.

This system explicitly rejects the busy, decorated register it replaced. No emoji as decoration competing with the content. No multi-stop gradients. No five-color pastel badge soup. No side-stripe accent borders. And nothing of the recipe-blog: no giant hero photos, no ad slots, no life-story preambles. If a surface looks like a generic SaaS dashboard, it has lost the warmth; if it looks like a food blog, it has lost the quiet. The target is between those: a warm, minimal, editorial-leaning tool.

**Key Characteristics:**
- Warm-neutral cream surfaces, never cold white, never pure black
- One terracotta accent, reserved for action, selection, and state
- A single optical serif (Fraunces) for names only; system sans for everything else
- Glanceable at arm's length: large body text, tabular figures, generous tap targets
- Precision over decoration; flat by default, motion only to convey state

## 2. Colors

A warm-neutral foundation tinted toward terracotta, with one saturated accent doing all the signalling.

### Primary
- **Terracotta** (`oklch(0.585 0.118 48)`): The single accent. Used for the active filter pill, focus rings, and selection only. Never decorative.
- **Terracotta Ink** (`oklch(0.500 0.118 46)`): A darkened cut of the accent used as *text* so it clears AA on cream, ingredient amounts, step numbers, the copy button label, recipe monograms.
- **Terracotta Tint** (`oklch(0.951 0.030 64)`): The accent at near-white lightness, for soft fills behind monograms, step numbers, and the active size-toggle press.

### Neutral
- **Ink** (`oklch(0.255 0.022 54)`): Primary text. A deep warm espresso, never `#000`.
- **Ink Secondary** (`oklch(0.440 0.028 52)`): Body prose inside cards, ingredient names.
- **Ink Muted** (`oklch(0.548 0.026 56)`): Labels, italian subtitles, category words, placeholders.
- **Cream Background** (`oklch(0.984 0.008 74)`): The page. Warm, soft, appetizing.
- **Surface** (`oklch(0.997 0.004 80)`): Cards, inputs, pills. A barely-warm off-white that lifts off the cream, never `#fff`.
- **Warm Fill** (`oklch(0.962 0.011 73)`): Quiet recessed blocks, tips, serve-time row, modal note.
- **Hairline** (`oklch(0.908 0.013 74)`) / **Divider** (`oklch(0.855 0.018 72)`): 1px borders and table rules.

### Tertiary (semantic, used sparingly)
- **Success** (`oklch(0.515 0.090 152)`): The copy button's confirmed state only.
- **QA Amber** (`oklch(0.498 0.072 70)`): The recipe QA-correction note only.

### Named Rules
**The One Accent Rule.** Terracotta is the only chromatic voice. It appears on action, selection, and state, nothing else. If two unrelated things on screen are both colored, one is wrong.

**The No-Pastel-Soup Rule.** Categories are distinguished by their word, not their hue. Every category label is the same muted ink. The five-color badge palette is forbidden.

## 3. Typography

**Display Font:** Fraunces (with Georgia, serif fallback)
**Body Font:** system-ui stack (-apple-system, Segoe UI)
**Label Font:** the same system sans, uppercase

**Character:** Fraunces is a soft, optical-size serif, warm and modern rather than formal or fashion-Didone; it carries the artisanal, appetizing note. The system sans does all the work of a tool: labels, controls, data, prose. The pairing is one editorial grace note over an honest, native interface.

### Hierarchy
- **Display** (500, 19px, 1.1, -0.01em): The app wordmark and modal title, in Fraunces.
- **Title** (500, 17px, 1.2, -0.01em): Recipe names, in Fraunces. They wrap rather than truncate.
- **Body** (400, 15px, 1.55): Method steps and ingredient names. Sized up from the old 13px for arm's-length reading.
- **Label** (600, 10px, +0.1em, uppercase): Section headers, category words, the Tip marker.
- **Amount** (600, 15px, tabular figures): Ingredient quantities in Terracotta Ink, right-aligned.

### Named Rules
**The Serif-For-Names-Only Rule.** Fraunces touches the wordmark and recipe names and nothing else. The instant it appears on a button, a label, or a data cell, it is misused, that is the system tipping into decoration.

**The Tabular-Figure Rule.** Every quantity uses `font-variant-numeric: tabular-nums` so amounts and batch sizes align in a column the eye can scan.

## 4. Elevation

Flat by default. Depth comes from tonal layering, surface lifting off cream, hairline borders, not from heavy shadow. Two whisper-soft shadows exist only to float cards and the modal off the page.

### Shadow Vocabulary
- **Card rest** (`box-shadow: 0 1px 2px oklch(0.30 0.02 55 / 0.045), 0 4px 18px oklch(0.30 0.02 55 / 0.055)`): The standing shadow under recipe cards, the guide card, and the active size toggle. Tinted warm, never neutral-gray.
- **Modal lift** (`box-shadow: 0 10px 44px oklch(0.28 0.02 55 / 0.16)`): The guide modal only.

### Named Rules
**The Tinted-Shadow Rule.** Shadows are warm (hue 55), never `rgba(0,0,0,...)`. A gray shadow on a cream surface reads cold and cheap.

## 5. Components

### Buttons
- **Shape:** Filter pills are fully round (`999px`); the copy button is gently rounded (`11px`).
- **Filter pill (default):** Surface background, Ink Secondary text, 1px hairline border, `8px 15px` padding.
- **Filter pill (active):** Solid Terracotta fill, Surface text, no border, no colored glow.
- **Copy button:** Surface background, Terracotta Ink text and 1px Terracotta Line border, with an inline copy SVG. On success it shifts to the Success color with a check icon and the word "Copied".
- **Hover / Focus / Active:** Transitions are color/background only, 150-200ms ease-out. Focus shows a 2.5px Terracotta `:focus-visible` ring offset 2px. Pressed pills tint to Warm Fill.

### Chips (category label)
- **Style:** Not a filled chip, a bare uppercase Ink Muted label at 10px / +0.1em. One treatment for every category.
- **QA badge:** The single exception, a small pill in QA Amber on a warm tint with a hairline border, marking corrected recipes.

### Cards / Containers
- **Corner Style:** `16px` radius.
- **Background:** Surface on the Cream page.
- **Shadow Strategy:** Card-rest shadow (see Elevation). Border firms from Hairline to Divider when open.
- **Border:** 1px Hairline.
- **Internal Padding:** `15px 16px` header; `16px` body, growing to `18px` bottom when expanded.
- **Disclosure:** Cards expand via an animated `grid-template-rows` 0fr→1fr at 240ms ease-out; the chevron rotates 180°.

### Inputs / Fields
- **Style:** Surface background, 1px Hairline border, `12px` radius, 16px text (no iOS zoom), an inline magnifier SVG inset left.
- **Focus:** Border shifts to Terracotta with a 3px Terracotta Tint glow.
- **Clear:** A round Warm Fill button appears at the right only when there is text.

### Navigation
- **Style:** A frosted sticky header, cream at 88% with a backdrop blur and a single hairline bottom border. The wordmark sits left in Fraunces; a quiet segmented size toggle (950 mL / 1.5 L) sits right, the active segment lifting on Surface with the card-rest shadow.

### Recipe Monogram (signature)
A `42px` Terracotta-Tint rounded tile holding the recipe's initial in Fraunces / Terracotta Ink. One consistent treatment gives the long list rhythm and a per-row anchor without resorting to emoji or per-item color.

## 6. Do's and Don'ts

### Do:
- **Do** keep terracotta to action, selection, and state; let the cream and ink carry the surface.
- **Do** set every quantity and batch size in tabular figures so columns align.
- **Do** size body and step text for arm's-length reading (15px floor) with generous tap targets.
- **Do** convey category by its word in one muted label color.
- **Do** keep surfaces flat, using warm tinted shadows and hairlines for the little depth there is.
- **Do** gate all motion behind `prefers-reduced-motion` and keep transitions 150-240ms ease-out.

### Don't:
- **Don't** use emoji as decoration where it competes with content; use inline stroke SVGs or a typographic monogram.
- **Don't** introduce multi-stop gradients on headers, cards, or modals.
- **Don't** bring back the five competing pastel category badges.
- **Don't** use a `border-left` (or `border-right`) greater than 1px as a colored accent stripe on tips, notes, or cards. Use a full-radius tinted block with a leading label.
- **Don't** use `#fff`, `#000`, or `rgba(0,0,0,...)`; every neutral is tinted warm in OKLCH.
- **Don't** let it drift toward a generic SaaS dashboard (cold, boxed, flat) or toward recipe-blog spam (giant hero, ads, life-story preamble, popups).
- **Don't** set Fraunces on buttons, labels, or data, names only.
