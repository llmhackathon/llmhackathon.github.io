# DESIGN.md — "Cobalt & Signal"

Swiss scientific-poster identity. Cobalt is literally an element and a pigment
born from materials chemistry — the site drenches its brand surfaces in flat
cobalt blue (International Klein Blue territory), prints content on true white
paper with near-black ink, and reserves **signal yellow** (the sodium D
emission line, 589 nm) for actions and accents. The emission-spectrum barcode
remains the brand mark: white ticks + yellow doublet on cobalt, full spectral
color on white.

## Theme

- **Register:** brand (marketing/event site) — design is the product.
- **Feel:** rigorous, energetic, communal. A screen-printed science poster, not a SaaS page and not a dark "hacker" site.
- **Surface strategy:** drenched — cobalt IS the brand surface (hero, page-header bands, footer, stats, callout panels). White paper carries reading. Yellow appears only where action or emphasis lives.

## Color (OKLCH, defined on `:root` in `_sass/_main.scss`)

| Token | Value | Role |
|---|---|---|
| `--void-deep` | `oklch(35% 0.2 263)` | deep cobalt (hero, footer, loader) |
| `--void` | `oklch(40% 0.21 263)` | cobalt band (page headers, stats, callouts) |
| `--void-panel` | `oklch(46% 0.21 263)` | panels on cobalt |
| `--paper` | `oklch(99.2% 0.002 263)` | content background (true white) |
| `--paper-dim` | `oklch(96.5% 0.009 263)` | alternate light surface |
| `--ink` | `oklch(18% 0.02 263)` | headings/body on light |
| `--ink-soft` | `oklch(38% 0.018 263)` | muted body on light (AA) |
| `--line` | `oklch(89% 0.01 263)` | hairlines on light |
| `--on-void` / `--on-void-soft` | 99% / 88% | text on cobalt |
| `--line-on-void` | `white / 0.28` | hairlines on cobalt |
| `--amber` | `oklch(88% 0.175 95)` | signal yellow — buttons, accents on cobalt |
| `--amber-ink` | `oklch(45% 0.24 264)` | the accent for text/links on white = **cobalt** |
| `--sp-*` | see scss | spectral line palette — thin lines on white only |

Rules: no gradients anywhere, no gradient text, no glassmorphism, no colored
side-stripes, **no decorative underlines** — links are cobalt at 500 weight and
underline only on hover. `h2 span` = solid cobalt word, nothing else.

## Typography

- **Display & body:** Inter (variable, optical sizing). Weights: 800 display, 700 headings, 400/500 body. Tight tracking at display sizes (-0.025em hero h1, -0.01em headings).
- **Data voice:** Martian Mono — timestamps, stats, badges, wavelength labels. It's a wide mono: keep sizes ≤0.95rem and letter-spacing ≤0.04em.
- Headings `text-wrap: balance`; body `text-wrap: pretty`, max 72ch.

## Signature components

- **Spectrum bar** (`_includes/spectrum.html`): real emission lines (H Balmer, Mg triplet, Na doublet). On cobalt contexts (`.page-header`, `.hero-spectrum`, `.footer-spectrum`) lines print white with the Na doublet in glowing yellow; on white they keep full spectral color. Ignites line-by-line on the hero (`spectrum--animated`).
- **Element tile** (`.element-tile`): white periodic-table tile, cobalt "Osi" symbol (three letters, deliberately not colliding with osmium's "Os"), hard offset shadow (`12px 12px 0`) — a screen-printed sticker on the cobalt hero.
- **Announce chip** (`.hero-announce`): yellow mono uppercase pill with pulsing dot — one per page maximum.
- **Stats band** (`.stats-band`): cobalt band, yellow mono values, white-alpha hairline separators.
- **Editions timeline** (`.edition-row`): hairline rows, mono years; upcoming edition in cobalt accent.
- **Cards**: flat white, 1px `--line` border, 8px radius; hover = cobalt border + small lift. No heavy shadows.
- **FAQ**: hairline-divided list with cobalt mono "Q" markers — not cards.
- **Buttons**: `.cta-button(-large)` signal yellow with ink text everywhere (cobalt and white surfaces alike); `.secondary-cta` outlined (white-on-cobalt, ink-on-white via `--light`). 4px radius.
- **Legacy banner** (`.legacy-banner`, in `_layouts/default.html`): fixed yellow strip glued to the viewport bottom on every page — "Formerly the LLM Hackathon for Applications in Materials and Chemistry". `body` reserves its height via `--legacy-banner-height`.

## Motion

- Hero: one staggered rise on load; spectrum ticks ignite with per-line delays.
- Scroll: `.reveal` + IntersectionObserver adds `.in-view`. Content fully visible without JS (`.js` gating) — never gate visibility on animation.
- Everything respects `prefers-reduced-motion: reduce`.

## Imagery

- `assets/images/recap-2025.png` — crystalline-lattice macro render in the cobalt/yellow palette (also the OG/social image).
- The hero is deliberately image-free: flat cobalt + type + tile IS the poster.
- Alt text written in the brand voice. No generic AI/robot/circuit imagery.

## Layout

- Content max-width 1160px; fluid `clamp()` section padding.
- z-index scale: nav 100 → overlay 110 → sidebar 120 → modal 200 → loader 300.
- Nav is white with ink links + yellow CTA; collapses ≤1350px into a cobalt sidebar.
