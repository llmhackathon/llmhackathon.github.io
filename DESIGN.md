# DESIGN.md — "Midnight & Aurora"

A night-sky scientific identity. Midnight navy carries the brand bands (hero,
page headers, footer), a soft warm-to-cool page ramp carries content, and the
accent system is role-separated: **action blue** for everything interactive,
the **aurora family** (periwinkle/violet/cyan) for data accents on midnight,
and **gold strictly honor-reserved** (awards, validated breakthroughs — the
Honor-Light rule; it also keeps the sodium-D doublet in the spectrum mark).

## Theme

- **Register:** brand (marketing/event site) — design is the product.
- **Feel:** rigorous, calm, credible. An observatory at dusk, not a SaaS page and not a dark "hacker" site.
- **Surface strategy:** committed — midnight bands anchor the brand moments; content sits on a soft #F6F6F2 → #DFE3EE ramp with white cards. Color roles are strict: blue = interactive, aurora = data, gold = honor.

## Color (defined on `:root` in `_sass/_main.scss`)

| Token | Value | Role |
|---|---|---|
| `--void-deep` | `#0D1226` | midnight-deep (hero, footer, loader) |
| `--void` | `#141C36` | midnight band (page headers, stats, callouts, legacy banner) |
| `--void-panel` | `#1D2A4F` | panels on midnight |
| `--bg-top/-mid/-bot` | `#F6F6F2 / #EDEDEA / #DFE3EE` | page background ramp (on `body`) |
| `--paper` | `#FFFFFF` | card/surface background |
| `--paper-dim` | `#EEF1F8` | cool inset paper (buttermilk-low) |
| `--ink` / `--ink-deep` | `#1E2A4A` / `#142042` | primary text ramp |
| `--ink-soft` / `--ink-subtle` | `#5C6470` / `#667085` | muted/tertiary text (AA) |
| `--line` | `rgba(186,193,214,.65)` | hairlines on light (glass edge) |
| `--on-void` / `--on-void-soft` | `#EEF1FB` / `#9AA7CD` | text on midnight |
| `--action(-hover/-pressed)` | `#3F5FBC / #314C98 / #263C79` | ALL interactive elements; text on it is `--cream` `#FFFDF8` |
| `--gold / --gold-soft / --ink-gold` | `#C79A4D / #EAD8AA / #7A4D14` | HONOR-RESERVED: award badges, prize highlights, the Na doublet |
| `--amber` / `--amber-bright` | `#8AA0E6 / #A9BBF0` | legacy token name = aurora periwinkle, data accents on midnight |
| `--amber-ink` | `#3F5FBC` | legacy token name = action blue, accent text on light |
| `--sp-*` | aurora family + gold + clay | spectrum lines: `#8B7CF6 #8AA0E6 #5EC9E8 #3FA3C4 #C79A4D #A66F44` |

Rules: no gradient text, no glassmorphism, no colored side-stripes, **no
decorative underlines** — links are action blue at 500 weight and underline
only on hover. `h2 span` = solid action-blue word. **Honor-Light Rule:** gold
never appears on buttons or generic accents; it marks honors only.

## Typography

- **Display & body:** Inter (variable, optical sizing). Weights: 800 display, 700 headings, 400/500 body. Tight tracking at display sizes (-0.025em hero h1, -0.01em headings).
- **Data voice:** Martian Mono — timestamps, stats, badges, wavelength labels. It's a wide mono: keep sizes ≤0.95rem and letter-spacing ≤0.04em.
- Headings `text-wrap: balance`; body `text-wrap: pretty`, max 72ch.

## Signature components

- **Spectrum bar** (`_includes/spectrum.html`): real emission lines (H Balmer, Mg triplet, Na doublet). On midnight contexts (`.page-header`, `.hero-spectrum`, `.footer-spectrum`) lines print white with the Na doublet in glowing gold; on light they use the aurora palette. Ignites line-by-line on the hero (`spectrum--animated`). Variants: `labeled=true` include param wraps it in `.spectrum-figure` with element + wavelength annotations (scientific notation keeps its case — Hβ, Mg, nm — never uppercased); `spectrum--interactive` brightens a line on hover (progressive enhancement only — never gate information on it); `spectrum--live` breathes the Na doublet on a 4s loop (reduced-motion gated, shimmer starts only after ignite ends).
- **Spectral strip** (`.spectral-strip`): a hairline-bounded interlude explaining the mark — labeled interactive spectrum + the `.spectral-atlas` plate. Built and styled but intentionally NOT used on the homepage: the explainer reads as spectroscopy content rather than event content. The spectrum stays a between-sections brand accent; keep the strip available for a future about/brand page.
- **Spectral ticks**: small 3px vertical bars keyed to the aurora palette before `.edition-year` and `.stat-value`. Intentional exception to the no-side-stripes rule: they are the spectrum motif at small scale (vertical emission lines), not card decoration; keep them ≤0.65em tall and never gold.
- **Element tile** (`.element-tile`): white periodic-table tile, action-blue "Osi" symbol (three letters, deliberately not colliding with osmium's "Os"), hard offset shadow (`12px 12px 0`) — a screen-printed sticker on the midnight hero.
- **Announce chip** (`.hero-announce`): periwinkle mono uppercase pill with pulsing dot — one per page maximum.
- **Stats band** (`.stats-band`): midnight band, periwinkle mono values, hairline separators.
- **Editions timeline** (`.edition-row`): hairline rows, mono years; upcoming edition in action-blue accent.
- **Cards**: flat white, 1px `--line` border, 8px radius; hover = action-blue border + small lift. No heavy shadows.
- **FAQ**: hairline-divided list with action-blue mono "Q" markers — not cards.
- **Buttons**: `.cta-button(-large)` action blue with cream text everywhere; hover `--action-hover`, pressed `--action-pressed`; `.secondary-cta` outlined (white-on-midnight, ink-on-light via `--light`). 4px radius.
- **Legacy banner** (`.legacy-banner`, in `_layouts/default.html`): fixed midnight strip glued to the viewport bottom on every page — "Formerly the LLM Hackathon for Applications in Materials and Chemistry". `body` reserves its height via `--legacy-banner-height`.

## Motion

- Hero: one staggered rise on load; spectrum ticks ignite with per-line delays.
- Scroll: `.reveal` + IntersectionObserver adds `.in-view`. Content fully visible without JS (`.js` gating) — never gate visibility on animation.
- Everything respects `prefers-reduced-motion: reduce`.

## Imagery

- `assets/images/recap-2025.png` — crystalline-lattice macro render in blue/gold (also the OG/social image).
- `assets/images/spectra/emission-atlas.svg` — midnight "Emission Atlas" plate: H / Mg / Na rows with glowing lines at true wavelengths over a 400–700 nm axis (used in the home spectral strip).
- `assets/images/spectra/spectrum-divider.svg` — slim transparent nine-line divider for light surfaces (available, unused by default).
- The hero is deliberately image-free: midnight + type + tile carries it.
- Alt text written in the brand voice. No generic AI/robot/circuit imagery.

## Layout

- Content max-width 1160px; fluid `clamp()` section padding.
- z-index scale: nav 100 → overlay 110 → sidebar 120 → modal 200 → loader 300.
- Nav is white with ink links + action-blue CTA; collapses ≤1350px into a midnight sidebar.
