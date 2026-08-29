---
version: beta
name: burhan-kapdawala-portfolio
description: A hand-drawn, sketchbook developer-portfolio system for a backend and platform engineer, in the spirit of posthog.com. Cream paper (#f8f4e8) holding near-black ink (#1d1b17), everything outlined in a 2px ink line with a hard offset shadow instead of blur. Outfit carries every narrative role at weights 500 to 800, Caveat handwriting is reserved for margin notes (org names, labels, the "now" flag, doodle captions), and Geist Mono stays on the technical layer (code, numbers, filenames). One loud accent, mustard yellow (#f6c453), plus a small box of crayons (sky, coral, leaf) that appears only inside illustrations and tinted cards. Headlines stay lowercase, sentence-case, and period-terminated. The copy voice (dry, specific, lowercase) is part of the brand and is never rewritten.

colors:
  canvas: "#f8f4e8"
  canvas-2: "#f3e7c6"
  surface: "#fffdf6"
  surface-2: "#f1eadb"
  surface-code: "#23211c"
  ink: "#1d1b17"
  body: "#3d3a33"
  muted: "#6b665b"
  line: "#1d1b17"
  line-soft: "#cfc7b3"
  accent: "#f6c453"
  accent-deep: "#e0a72a"
  accent-soft: "#fbe6ad"
  on-accent: "#1d1b17"
  sky: "#9fd3dd"
  coral: "#ee8264"
  leaf: "#7fae6f"
  navy: "#33406b"
  code-text: "#f3eee0"
  code-muted: "#9a9384"
  selection-bg: "#f6c453"
  selection-fg: "#1d1b17"
  dark-canvas: "#1c1a16"
  dark-canvas-2: "#23201a"
  dark-surface: "#2a2721"
  dark-surface-2: "#322e27"
  dark-surface-code: "#15140f"
  dark-ink: "#f3eee0"
  dark-body: "#cfc8b8"
  dark-muted: "#a39c8b"
  dark-line: "#f3eee0"
  dark-line-soft: "#4a453b"
  dark-shadow: "#0b0a08"

typography:
  display-lg:
    fontFamily: Outfit, ui-rounded, ui-sans-serif, system-ui, sans-serif
    fontSize: clamp(40px, 25.6px + 3vw, 64px)
    fontWeight: 800
    lineHeight: 1.02
    letterSpacing: -0.03em
  display-md:
    fontFamily: Outfit, ui-rounded, ui-sans-serif, system-ui, sans-serif
    fontSize: clamp(32px, 24px + 1.6vw, 44px)
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: -0.02em
  display-sm:
    fontFamily: Outfit, ui-rounded, ui-sans-serif, system-ui, sans-serif
    fontSize: clamp(24px, 20.8px + 0.7vw, 30px)
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: -0.02em
  title:
    fontFamily: Outfit, ui-rounded, ui-sans-serif, system-ui, sans-serif
    fontSize: 19px
    fontWeight: 700
    lineHeight: 1.2
  body-lg:
    fontFamily: Outfit, ui-rounded, ui-sans-serif, system-ui, sans-serif
    fontSize: 19px
    fontWeight: 400
    lineHeight: 1.6
  body-md:
    fontFamily: Outfit, ui-rounded, ui-sans-serif, system-ui, sans-serif
    fontSize: 17px
    fontWeight: 400
    lineHeight: 1.6
  body-sm:
    fontFamily: Outfit, ui-rounded, ui-sans-serif, system-ui, sans-serif
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.6
  nav-link:
    fontFamily: Outfit, ui-rounded, ui-sans-serif, system-ui, sans-serif
    fontSize: 17px
    fontWeight: 600
    lineHeight: 1
  button:
    fontFamily: Outfit, ui-rounded, ui-sans-serif, system-ui, sans-serif
    fontSize: 17px
    fontWeight: 700
    lineHeight: 1
  hand:
    fontFamily: Caveat, Comic Sans MS, Chalkboard SE, cursive
    fontSize: 22px
    fontWeight: 600
    lineHeight: 1.1
  mono-md:
    fontFamily: Geist Mono, ui-monospace, SF Mono, Menlo, monospace
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.75
  stat:
    fontFamily: Outfit, ui-rounded, ui-sans-serif, system-ui, sans-serif
    fontSize: clamp(32px, 24px + 1.6vw, 44px)
    fontWeight: 800
    lineHeight: 1.05
    letterSpacing: -0.03em

rounded:
  inline: 6px
  control: 999px
  panel: 16px

spacing:
  1: 4px
  2: 8px
  3: 12px
  4: 16px
  5: 24px
  6: 32px
  7: 48px
  8: 64px
  section: clamp(64px, 48px + 4vw, 104px)
  container: 1056px
  measure: 62ch
  nav-height: 72px

components:
  line:
    stroke: "2px solid {colors.line} on every drawn edge: cards, buttons, tags, the terminal, the theme toggle, illustration outlines (2.5 in SVG)"
    soft: "2px dashed {colors.line-soft} between sections and table rows"
  shadow:
    style: "hard offset in ink, no blur: 2px 2px (shadow-1), 4px 4px (shadow-2), 6px 6px (shadow-3)"
    hover: "element translates -1px -1px and the shadow grows by 1px"
    active: "element translates onto the shadow and the shadow collapses to 0"
  nav-bar:
    height: "{spacing.nav-height}"
    brand: "a yellow disc with an ink line and a handwritten 'b', plus the name in Outfit 800; the disc tilts -12deg on hover"
    links: "{typography.nav-link} in muted; the current page in ink with a hand-drawn yellow squiggle underneath"
  theme-toggle:
    size: 38px
    shape: "ink-lined circle; a yellow sun disc that becomes a crescent moon in dark"
  button-primary:
    backgroundColor: "{colors.accent}"
    textColor: "{colors.on-accent}"
    height: 44px
    rounded: "{rounded.control}"
    border: "{components.line.stroke}"
    shadow: "shadow-2, with the hover lift and press collapse"
  button-secondary:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    same: "line, shadow, and physics as primary"
  button-sm:
    height: 36px
    shadow: "shadow-1"
  card:
    backgroundColor: "{colors.surface}"
    border: "{components.line.stroke}"
    rounded: "{rounded.panel}"
    shadow: "shadow-2"
    variants: "card--yellow, card--sky, card--coral, card--paper. tinted cards re-scope the ink ladder to dark ink so text stays readable in both themes"
  marker:
    style: "a skewed yellow run behind one key phrase in the h1 (light); a thick yellow underline in dark"
  terminal:
    frame: "card with a paper title bar: three crayon dots (coral, yellow, leaf), the context name, a handwritten cluster shape right-aligned"
    body: "{colors.surface-code} inside, {typography.mono-md}; prompt in accent, output in sky"
    note: "the inside stays dark in both themes; the frame follows the theme"
  timeline:
    layout: "dashed ink line down the left; a 16px ink-lined dot per role, filled yellow for the current one"
    label: "org name in {typography.hand}; the 'now' flag is a tiny yellow pill tilted -3deg"
  trio:
    layout: "3fr 2fr grid at >=768px with a full-width third card; plain card, yellow card, sky card"
  stat-card:
    number: "{typography.stat}, tabular figures; unit inline in {typography.hand} muted"
    label: "{typography.body-sm}"
    hero: "the zero-loss stat is a yellow card tilted -1.2deg"
  sparkle:
    use: "a three-star yellow doodle before every home-page section title; twinkles once on reveal"
  steps:
    marker: "numbered yellow discs in {typography.hand}, alternately tilted -6deg / 5deg"
  files:
    layout: "three index cards, the first tinted accent-soft, the others rotated 0.8deg and -0.7deg"
  compare:
    layout: "two stat cards with a handwritten 'vs' between them; the fast one is sky"
  table:
    frame: "card; caption in {typography.hand} on accent-soft; header row on surface-2 with an ink rule; dashed rules between rows"
  empty-state:
    style: "dashed ink card with ruled notebook lines and a pencil doodle"
  footer:
    band: "canvas-2 bleeds to the viewport edges with a 2px ink line on top; links are small pill buttons; tagline in {typography.hand}"
  grain:
    style: "fixed, click-through SVG turbulence overlay at 35% (multiply) in light, 50% (screen) in dark"

illustrations:
  style: "flat fills from the crayon palette with 2.5px ink outlines, rounded corners, tiny dot eyes and a smile. no gradients, no shading."
  hero: "three server nodes on a shelf (sky, yellow, coral); the yellow one wears a crown because it is the leader; dashed replication arcs between them"
  thoughts: "a pencil that has drawn a short squiggle and stopped"
  raftkv: "the architecture diagram: coral client with a face, accent-soft engine, sky sidecar, dashed node frames, handwritten arrow labels"
---

## Overview

This is the design system for burhankapadia18.github.io/portfolio: a three-page static site (about, thoughts, raftkv) for a backend and platform engineer. It borrows its posture from posthog.com and the allwhere.co homepage: everything looks drawn onto cream paper with a fat ink pen, colours are flat and few, shadows are hard offsets rather than blur, and the page has a sense of humour without being noisy.

The system still reads as an engineering document (real terminal commands, real benchmark figures, a real architecture diagram), it just happens to be one with doodles in the margins. Hierarchy comes from size and weight on a single rounded sans; the ink line and the yellow do the rest.

**Key Characteristics:**

- Cream canvas (`{colors.canvas}`) and near-black ink (`{colors.ink}`). Never pure white, never pure black.
- Every container is outlined in a 2px ink line and sits on a hard offset shadow. There is no blur anywhere on the site.
- Outfit carries every narrative role at 400 to 800. Caveat is for margin notes only. Geist Mono is for code, numbers, filenames, and table cells. Body copy is never mono or handwritten.
- One accent, mustard yellow. It is the primary button, the marker behind the hero phrase, the crown, the current-role dot, the "now" flag, the sparkles, the step numbers, and the yellow card variant.
- Three crayons (sky, coral, leaf) exist for illustrations and tinted cards. They never colour text and never appear in the chrome.
- Pills for every control, 16px on every card, 6px on inline code. Nothing else.
- A subtle paper grain sits over the whole page as a fixed overlay.
- Headlines are lowercase, sentence-case, and period-terminated. Section headings on article pages drop the period.
- The copy voice is preserved verbatim through redesigns.

## Colors

### Paper and Ink

`{colors.canvas}` is the page floor; `{colors.surface}` is the card face and the terminal title bar; `{colors.surface-2}` is the inset tone for inline code, table headers, and the shelf board; `{colors.canvas-2}` is the footer band. Text runs a three-step ladder: `{colors.ink}` for headings, links, strong text, and stat numbers; `{colors.body}` for paragraphs; `{colors.muted}` for labels, captions, and nav links at rest.

### Accent and Crayons

`{colors.accent}` is the only chromatic colour allowed in the chrome. `{colors.sky}`, `{colors.coral}`, and `{colors.leaf}` are the illustration palette: the three nodes on the shelf, the terminal's window dots, the client in the diagram, the pencil eraser. Sky and coral also exist as card tints (`card--sky`, `card--coral`). Tinted cards re-scope `--ink`, `--body`, and `--muted` to dark values so their text stays dark in both themes.

### Dark theme

Dark mode swaps the paper for warm charcoal (`{colors.dark-canvas}`) and the ink for cream (`{colors.dark-ink}`). The 2px line becomes cream too, so cards look like chalk drawings; the hard shadow drops to `{colors.dark-shadow}`. Yellow stays yellow. The terminal's inside stays dark in both themes. The initial theme is applied inline in `<head>` so there is no flash, and the toggle persists in `localStorage`.

## Typography

Outfit (400, 500, 600, 700, 800), Caveat (500, 600, 700), and Geist Mono (400, 500), loaded from Google Fonts with `display=swap`. Three families with three distinct jobs: narrative, margin notes, technical.

`{typography.display-lg}` is used once per page for the h1. `{typography.display-md}` is the home section headline, `{typography.display-sm}` the article section headline and the trio's statement. `{typography.title}` is the h3 for roles and project names. Body runs at 17px with a 19px lede.

### Principles

- **Weight is allowed to shout.** The h1 is 800, section heads 700. Body stays 400.
- **Handwriting is a margin note, not a headline.** Org names, dt labels, table captions, diagram arrow labels, the footer tagline. Never a paragraph, never a heading.
- **Mono marks "this is technical."** Numbers in tables, commands, filenames, ports. Stat numbers are Outfit 800 because they are display, not data.
- **Sentence case, lowercase, period-terminated headlines.** No uppercase eyebrows, no numbering prefixes.

## Layout

4px base. Sections are separated by `{spacing.section}` and a dashed soft line. The home page is contained at `{spacing.container}`; long-form pages sit in a 46rem article column with a `{spacing.measure}` cap on paragraphs. The hero is a 6/5 split at 896px and above with the shelf illustration overlapping the top of the terminal. The trio is a `3fr 2fr` grid with a full-width third card. The featured project is a 7/5 split with a stack of stat cards. Everything collapses to one column below 640px.

## Elevation and Depth

One method: the hard offset shadow (`shadow-1` on small controls and tags, `shadow-2` on buttons and cards, `shadow-3` on the terminal). Interactive elements lift toward the top-left on hover and press down onto their shadow on click. A few cards are deliberately tilted a degree or so (the zero-loss stat, two of the durability index cards) so the layout reads as pinned to a board rather than generated.

## Shapes

Pills on buttons, tags, the "now" flag, and footer links. 16px on cards, the terminal, the diagram, the table frame, and the empty state. 6px on inline code. Circles on the brand badge, the theme toggle, timeline dots, and step numbers.

## Motion

Hero elements cascade in with a 70ms stagger and a half-degree of rotation (`.rise`); below-fold sections reveal once via IntersectionObserver (`.reveal`) and their sparkle twinkles once. Buttons, cards, and the toggle use the lift/press physics above. Everything collapses to instant under `prefers-reduced-motion: reduce`. Only `transform` and `opacity` are animated.

## Do's and Don'ts

### Do

- Draw every container with the 2px line and a hard shadow. If it has an edge, it has ink.
- Keep the accent yellow and let the crayons live only in drawings and tinted cards.
- Use Caveat for notes in the margin and nowhere else.
- Put real content in the terminal and real numbers in the stats.
- Give new illustrations faces, flat fills, and ink outlines. Keep them small and specific to the content next to them.
- Test both themes. The dark theme is chalk on a blackboard, not a filter.

### Don't

- Don't add blur shadows, gradients (other than the marker run), glows, or a second accent.
- Don't put a dark section on the cream page. The terminal's inside is the one exception.
- Don't use em-dashes or en-dashes in visible copy.
- Don't use emoji or icon fonts. Everything drawn is an inline SVG or CSS.
- Don't mix radii: pills, 16px, 6px.
- Don't set body paragraphs in mono or handwriting.
- Don't rewrite the copy. Lowercase, dry, specific.

## Responsive Behavior

640px (`40rem`): timeline gains its label column, footer, files grid, comparison, and "elsewhere" go multi-column. 768px (`48rem`): the trio and featured project split. 896px (`56rem`): the hero splits 6/5. The nav collapses the brand to its badge below 480px. The architecture diagram keeps a 620px minimum width and scrolls inside its card on narrow screens.

Touch targets: buttons are 44px tall (36px for the small variant), nav links have 8px vertical padding, the theme toggle is 38px.

## Known Gaps

- The thoughts page has no posts yet, so there is no article-list component. When writing exists, reuse the timeline pattern (handwritten date left, title and standfirst right).
- There is no photography treatment. If a photo is added, frame it as a card with the ink line and shadow-2.
