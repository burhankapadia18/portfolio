---
version: alpha
name: burhan-kapdawala-portfolio
description: A quiet developer-portfolio system for a backend and platform engineer. Near-white canvas (#fafafa) holding near-black ink (#171717), Geist for everything narrative at weight 500 for display and 400 for body, Geist Mono reserved for the technical layer (labels, numbers, code, tags). One accent, a rust orange (#c2410c light / #fb923c dark), used only on the current-page marker, the terminal prompt, focus rings, and the "now" flag. Depth comes from hairlines and one dark code surface that stays dark in both themes; there are no drop shadows heavier than a stacked 4-6% micro-shadow. Headlines are lowercase, sentence-case, and period-terminated. The voice of the copy (dry, specific, lowercase) is part of the brand and is never rewritten.

colors:
  canvas: "#fafafa"
  surface: "#ffffff"
  surface-2: "#f2f2f2"
  surface-code: "#171717"
  ink: "#171717"
  body: "#4a4a4a"
  muted: "#6f6f6f"
  hairline: "#e6e6e6"
  hairline-strong: "#c9c9c9"
  accent: "#c2410c"
  accent-hover: "#9a3412"
  accent-soft: "rgba(194, 65, 12, 0.08)"
  on-accent: "#ffffff"
  code-text: "#ededed"
  code-muted: "#8a8a8a"
  selection-bg: "#171717"
  selection-fg: "#fafafa"
  dark-canvas: "#0a0a0a"
  dark-surface: "#111111"
  dark-surface-2: "#181818"
  dark-surface-code: "#0f0f0f"
  dark-ink: "#ededed"
  dark-body: "#a8a8a8"
  dark-muted: "#8a8a8a"
  dark-hairline: "#262626"
  dark-hairline-strong: "#3d3d3d"
  dark-accent: "#fb923c"
  dark-accent-hover: "#fdba74"

typography:
  display-lg:
    fontFamily: Geist, ui-sans-serif, system-ui, sans-serif
    fontSize: clamp(34px, 24px + 2.2vw, 48px)
    fontWeight: 500
    lineHeight: 1.08
    letterSpacing: -0.035em
  display-md:
    fontFamily: Geist, ui-sans-serif, system-ui, sans-serif
    fontSize: clamp(28px, 22px + 1.2vw, 36px)
    fontWeight: 500
    lineHeight: 1.25
    letterSpacing: -0.02em
  display-sm:
    fontFamily: Geist, ui-sans-serif, system-ui, sans-serif
    fontSize: clamp(22px, 19px + 0.6vw, 26px)
    fontWeight: 500
    lineHeight: 1.25
    letterSpacing: -0.02em
  title:
    fontFamily: Geist, ui-sans-serif, system-ui, sans-serif
    fontSize: 18px
    fontWeight: 500
    lineHeight: 1.25
    letterSpacing: -0.01em
  body-lg:
    fontFamily: Geist, ui-sans-serif, system-ui, sans-serif
    fontSize: 18px
    fontWeight: 400
    lineHeight: 1.6
  body-md:
    fontFamily: Geist, ui-sans-serif, system-ui, sans-serif
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.6
  body-sm:
    fontFamily: Geist, ui-sans-serif, system-ui, sans-serif
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.6
  nav-link:
    fontFamily: Geist, ui-sans-serif, system-ui, sans-serif
    fontSize: 14px
    fontWeight: 500
    lineHeight: 1
  button:
    fontFamily: Geist, ui-sans-serif, system-ui, sans-serif
    fontSize: 14px
    fontWeight: 500
    lineHeight: 1
  mono-md:
    fontFamily: Geist Mono, ui-monospace, SF Mono, Menlo, monospace
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.75
  mono-label:
    fontFamily: Geist Mono, ui-monospace, SF Mono, Menlo, monospace
    fontSize: 12px
    fontWeight: 400
    lineHeight: 1.4
  mono-stat:
    fontFamily: Geist Mono, ui-monospace, SF Mono, Menlo, monospace
    fontSize: clamp(28px, 22px + 1.2vw, 36px)
    fontWeight: 500
    lineHeight: 1.1
    letterSpacing: -0.02em

rounded:
  inline: 4px
  control: 6px
  panel: 10px

spacing:
  1: 4px
  2: 8px
  3: 12px
  4: 16px
  5: 24px
  6: 32px
  7: 48px
  8: 64px
  section: clamp(64px, 48px + 4vw, 96px)
  container: 1024px
  measure: 62ch
  nav-height: 64px

components:
  nav-bar:
    height: "{spacing.nav-height}"
    borderBottom: "1px solid {colors.hairline}"
    brand: "{typography.title} at 16px, ink"
    links: "{typography.nav-link}, muted; current page in ink with a 2px accent underline"
  theme-toggle:
    size: 32px
    rounded: "{rounded.control}"
    border: "1px solid {colors.hairline}"
    glyph: "a half-filled 13px disc drawn in CSS; rotates 180deg when the theme flips"
  button-primary:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.canvas}"
    height: 40px
    rounded: "{rounded.control}"
    hover: "translateY(-1px) + shadow-2"
    active: "translateY(1px) scale(0.98)"
  button-secondary:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    border: "1px solid {colors.hairline}"
    rounded: "{rounded.control}"
    hover: "surface-2 background, hairline-strong border"
  button-sm:
    height: 32px
    typography: "{typography.mono-label}"
  code-panel:
    backgroundColor: "{colors.surface-code}"
    border: "1px solid rgba(255,255,255,0.1)"
    rounded: "{rounded.panel}"
    bar: "{typography.mono-label} in code-muted, hairline below"
    prompt: "{colors.accent}"
    note: "stays dark in both themes; the only inverted surface on any page"
  experience-row:
    layout: "grid 11rem 1fr at >=640px; stacked below"
    label: "{typography.mono-md} in muted; the current role carries a 'now' flag in accent"
    divider: "one hairline per row, bottom only"
  trio-cell:
    padding: "{spacing.5}"
    border: "1px solid {colors.hairline}"
    rounded: "{rounded.panel}"
    variants: "plain surface / accent-soft tint / surface-2; 2fr 1fr grid with a full-width third cell"
  stat:
    number: "{typography.mono-stat} in ink, tabular figures"
    unit: "14px mono in muted, inline after the number"
    label: "{typography.body-sm} in muted"
    divider: "hairline on top"
  tag:
    typography: "{typography.mono-label}"
    border: "1px solid {colors.hairline}"
    rounded: "{rounded.control}"
    padding: "2px 8px"
  table:
    typography: "{typography.mono-md} at 14px, tabular figures"
    header: "14px sans, weight 500, muted, hairline-strong rule below"
    rows: "single hairline between rows, none after the last"
  empty-state:
    border: "1px dashed {colors.hairline-strong}"
    rounded: "{rounded.panel}"
    padding: "{spacing.6}"
  footer:
    borderTop: "1px solid {colors.hairline}"
    layout: "contact line left, links right, mono tagline full width"
---

## Overview

This is the design system for burhankapadia18.github.io/portfolio. It is a three-page static site (about, thoughts, raftkv) for a backend and platform engineer, and it borrows its posture from the developer-tools brands in `design-md/`: Vercel's ink-on-near-white duet and mono-for-the-technical-layer rule, Cursor's calm weight-500 display and hairline-only depth, Supabase's square-ish 6px controls and single accent, and opencode.ai's idea that one real terminal surface is the only visual moment a page needs.

The system reads as a well-typeset engineering document. Nothing on the page is decorative for its own sake: the one accent marks state (current page, the prompt, focus, "now"), the one dark panel holds real commands from a real project, and hierarchy comes from size and weight on a single sans, not from color or ornament.

**Key Characteristics:**

- Near-white canvas (`{colors.canvas}`) and near-black ink (`{colors.ink}`). Never pure white, never pure black.
- Geist carries every narrative role. Geist Mono carries the technical layer only: labels, numbers, code, tags, table cells. Body copy is never mono.
- Display weight is 500. Nothing on the site is bolder than 500.
- One accent, rust orange, used on state only. It is never a background, never a headline color, never a decoration.
- Depth is a hairline (`{colors.hairline}`) or a two-step surface ladder. The only shadows are stacked 3-6% micro-offsets on buttons and the code panel.
- One radius system: 6px on controls and tags, 10px on panels, 4px on inline code.
- Headlines are lowercase, sentence-case, and period-terminated ("experience.", "hire me.", "raftkv."). Section headings on article pages drop the period.
- The copy voice is lowercase, dry, specific, and occasionally funny. It is preserved verbatim through redesigns.

## Colors

### Canvas and Ink

`{colors.canvas}` is the page floor; `{colors.surface}` is used for cards, the secondary button, and the diagram panel; `{colors.surface-2}` is the inset tone for the benchmark comparison panel, inline code, and the wide "hire me" cell. Text runs a three-step ladder: `{colors.ink}` for headings, links, strong text, and stat numbers; `{colors.body}` for paragraphs; `{colors.muted}` for labels, captions, nav links at rest, and table headers.

### Accent

`{colors.accent}` appears in exactly these places: the underline on the current nav item, the `$` prompt in code panels, the "now" flag on the current role, the focus ring, the engine box in the architecture diagram, step numbers on the write path, and link hover. `{colors.accent-soft}` tints one cell in the "hire me" trio. That is the full list. Adding a second chromatic color anywhere breaks the system.

### Dark theme

Dark mode swaps the tokens under `[data-theme="dark"]`: canvas `{colors.dark-canvas}`, ink `{colors.dark-ink}`, accent lifted to `{colors.dark-accent}` so it clears WCAG AA on the dark floor. The code panel does not flip; it uses `{colors.dark-surface-code}` and stays a dark surface with a hairline ring. Both themes are first-class and the toggle persists in `localStorage`; the initial theme is applied inline in `<head>` so there is no flash.

## Typography

### Font Family

Geist (400, 500) and Geist Mono (400, 500), loaded from Google Fonts with `display=swap`, with `ui-sans-serif` / `ui-monospace` system fallbacks. Two families, four weights, nothing else.

### Hierarchy

`{typography.display-lg}` is used once per page, for the h1. `{typography.display-md}` is the home-page section headline, `{typography.display-sm}` the article section headline and the statement inside the trio's lead cell. `{typography.title}` is the h3 for roles and project names. Body runs at 16px with an 18px lede variant for hero subtext and article standfirsts.

### Principles

- **Weight 500 is the ceiling.** Hierarchy is built from size and color, not boldness.
- **Negative tracking on display only.** -0.035em on the h1, -0.02em on section heads, none on body.
- **Mono marks "this is technical."** If a string is a number, a filename, a command, a tag, or a label that describes structure, it is mono. If it is a sentence, it is sans.
- **Sentence case, lowercase, period-terminated headlines.** Never uppercase, never title case, no tracked-out small-caps eyebrows.
- **Tabular figures on every number.** Stats and table cells use `font-variant-numeric: tabular-nums`.

## Layout

### Spacing System

4px base. Component padding uses `{spacing.4}` and `{spacing.5}`; sections are separated by `{spacing.section}` (64-96px fluid) and a single hairline. The home page is contained at `{spacing.container}`; long-form pages (raftkv, thoughts) sit in a 46rem article column with a `{spacing.measure}` cap on paragraphs.

### Grid

The hero is a 7/5 split at 896px and above, stacked below. Experience rows are an 11rem label column plus content. The "hire me" trio is a `2fr 1fr` grid with a full-width third cell. The featured project is a 7/5 split with a vertical stat rail (label left, mono number right). Every multi-column layout collapses to one column below 640px; nothing relies on flex percentage math.

### Whitespace Philosophy

Sections breathe at 64-96px but rows inside them are tight (24px). The hero's top padding is capped at 88px so the headline and CTAs always sit in the first viewport.

## Elevation and Depth

Three levels, in order of preference: a hairline, a surface step (`{colors.surface}` on `{colors.canvas}`, or `{colors.surface-2}` inset), and finally the stacked micro-shadow (`shadow-1` on secondary buttons, `shadow-2` on the code panel and primary-button hover). There are no glows, no gradients, no grain, and no skewed "second sheet" tricks.

## Shapes

`{rounded.control}` (6px) on buttons, tags, the theme toggle, and diagram boxes. `{rounded.panel}` (10px) on the code panel, trio cells, the diagram frame, the comparison panel, and the empty state. `{rounded.inline}` (4px) on inline code and focus rings. Pills do not exist in this system.

## Components

**Nav bar.** 64px, hairline below, brand left in ink, links right in muted with the current page in ink and a 2px accent underline. The theme toggle is a 32px hairline square containing a half-filled disc drawn in CSS; it rotates on flip.

**Buttons.** Primary is ink-filled with canvas text; secondary is surface with a hairline and `shadow-1`. Both lift 1px on hover and press 1px on active. The small mono variant is used for article meta links only.

**Code panel.** The one dark surface. A mono bar names the context ("raftkv", "shell") and the cluster shape; the body is real, runnable commands. The prompt is the only accent inside it.

**Experience row.** Mono organisation label on the left (with an accent "now" flag on the current role), sans title and paragraph on the right, one hairline under each row.

**Trio cells.** Three cells in a 2fr / 1fr / full-width arrangement: a plain statement cell, an accent-soft tinted definition list, and a surface-2 two-column prose cell. Exactly three cells for three ideas; never pad to a fourth.

**Stats.** Mono display number, inline mono unit, sans label, hairline above. Used for the raftkv figures on the home page and the read-cost comparison on the article page.

**Table.** Mono cells with tabular figures, sans muted header, a strong hairline under the header and a light hairline between rows only.

**Empty state.** Dashed hairline panel with the honest copy and one secondary action. Used on thoughts until there is writing.

## Do's and Don'ts

### Do

- Keep display weight at 500 and body at 400. Use size and ink/muted contrast for hierarchy.
- Use mono for anything that is a number, command, filename, tag, or structural label.
- Put real content in the code panel: commands that actually work against the raftkv repo.
- Separate sections with a single hairline and 64-96px of air.
- Keep the accent on state (current, prompt, focus, now). One accent, everywhere it appears.
- Preserve the copy voice. Lowercase, dry, specific. Rewrites are a content decision, not a design one.
- Test both themes; the dark theme is not a filter over the light one.

### Don't

- Don't add a second chromatic color, a gradient, a glow, grain, or a background pattern.
- Don't use uppercase tracked-out eyebrows, section numbers, or "01 /" style prefixes above headings.
- Don't use em-dashes or en-dashes in visible copy. Periods, commas, colons, and parentheses do the work.
- Don't use emoji or hand-drawn SVG icons in the chrome. The theme toggle disc is the only glyph.
- Don't invert a content section to dark in the light theme (or vice versa). The code panel is the single exception and it is the same in both themes.
- Don't add a pill radius. 6px controls, 10px panels.
- Don't fake product UI, log output, or numbers. Every figure on the site comes from the raftkv benchmarks doc.
- Don't set body paragraphs in mono, and don't set numbers in the sans.

## Responsive Behavior

### Breakpoints

640px (`40rem`): experience rows, footer, files grid, comparison panel, and the "elsewhere" pair go multi-column. 768px (`48rem`): the trio and featured project split. 896px (`56rem`): the hero splits 7/5. The nav is a single row from 480px up and wraps to brand-over-links below that.

### Touch Targets

Buttons are 40px tall (32px for the small mono variant); nav links have 8px vertical padding; the theme toggle is 32px square.

### Motion

Hero elements cascade in with a 70ms stagger (`.rise`); below-fold sections reveal once via IntersectionObserver (`.reveal`). Buttons translate 1px on hover and scale 0.98 on press. Everything collapses to instant under `prefers-reduced-motion: reduce`. Only `transform` and `opacity` are animated.

## Known Gaps

- The thoughts page has no posts yet, so there is no article-list component. When writing exists, use the experience-row pattern (mono date left, title and standfirst right).
- There is no image treatment defined because the site has no photography. If one is added, frame it in `{rounded.panel}` with a hairline and no shadow.
