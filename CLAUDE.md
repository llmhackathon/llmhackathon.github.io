# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **Jekyll-powered static website** for the **Open Scientific Intelligence (OSI) Hackathon for the Physical Sciences & Mathematics** (formerly the LLM Hackathon for Materials Science & Chemistry, renamed for the October 21–22, 2026 edition to cover LLMs, agents, datasets, models, and scientific software across the physical sciences and mathematics) - an international hybrid hackathon event. The website serves as the main information hub for participants, organizers, and site hosts. Historical pages (2023-2025 projects/awards) intentionally keep the old "LLM Hackathon" name.

## Architecture

### Jekyll Structure

- **Static Site Generator**: Uses Jekyll for modular, maintainable code
- **GitHub Pages Compatible**: Builds automatically on GitHub Pages without additional configuration
- **Data-Driven**: Content managed through YAML data files for easy updates
- **Modular Templates**: Reusable layouts and includes for consistent design
- **Sass Processing**: Organized, modular CSS with variables and nesting

### Directory Structure

```
├── _config.yml              # Jekyll configuration
├── _layouts/                 # Page templates
│   ├── default.html         # Base layout with navigation/footer
│   ├── home.html            # Homepage layout
│   ├── page.html            # Standard page layout
│   └── site-location.html   # Location-specific page layout
├── _includes/               # Reusable components
│   ├── head.html           # Meta tags, CSS includes
│   ├── navigation.html     # Site navigation
│   ├── footer.html         # Site footer
│   ├── loader.html         # Loading animation
│   └── scripts.html        # JavaScript functionality
├── _data/                   # Structured content
│   ├── navigation.yml      # Navigation items
│   ├── sponsors.yml        # Sponsor information
│   ├── team.yml           # Team member data
│   ├── schedule.yml       # Event schedule
│   ├── prizes.yml         # Prize information
│   └── faq.yml            # FAQ items
├── _sass/                   # Modular Sass files
│   └── _main.scss          # Main stylesheet
├── _sites/                  # Location-specific pages
│   └── berlin.md           # Example location page
├── assets/                  # Static assets
│   ├── css/main.scss       # Sass entry point
│   └── images/             # Image files
└── *.md                    # Content pages (index, about, etc.)
```

### Key Pages

- `index.html` - Main landing page with hero section, countdown timer, and key information
- `about.html` - Event details and mission
- `projects.html` - Showcase of previous hackathon projects with links to repositories
- `resources.html` - Comprehensive learning materials, datasets, and research papers
- `sites.html` - List of on-site locations worldwide
- `sites/*.html` - Individual pages for each hackathon location
- `sponsors.html` - Partner and sponsor information
- `submission.html` - Project submission guidelines
- `faq.html` - Frequently asked questions

### Styling Architecture

- **Design system**: "Cobalt & Signal" — see `DESIGN.md` for the full spec. No CSS framework (Tailwind was removed); everything lives in `_sass/_main.scss` as OKLCH design tokens on `:root`.
- **Typography**: Archivo (display + body, expanded widths for headings) and Martian Mono (data voice: stats, timestamps, badges) from Google Fonts
- **Color Scheme**: Flat drenched cobalt (`--void*`) + true-white paper (`--paper*`), with signal yellow (`--amber`) as the single action color and cobalt (`--amber-ink`) as the text accent on white; emission-spectrum motif prints white+yellow on cobalt, full color on white. No gradients, no decorative underlines (links underline on hover only)
- **Signature components**: spectrum bar include (`_includes/spectrum.html`), element tile, stats band, editions timeline
- **Responsive Design**: fluid `clamp()` spacing/type, `auto-fit minmax()` grids, nav collapses ≤1350px
- **Motion**: scroll reveals + hero entrance, all gated behind `prefers-reduced-motion`

## Development Commands

### Jekyll Development

Local dev requires Ruby 3.4 (the `github-pages` gem is not compatible with Ruby 4.x).
Homebrew `ruby@3.4` is installed and exported in `~/.zshrc`:

```bash
# ~/.zshrc already contains:
# export PATH="/opt/homebrew/opt/ruby@3.4/bin:$PATH"
# export PATH="$(/opt/homebrew/opt/ruby@3.4/bin/gem environment gemdir)/bin:$PATH"
```

```bash
# Install Jekyll and dependencies
bundle install

# Serve the website locally (with auto-rebuild)
bundle exec jekyll serve

# Serve with live reload and drafts
bundle exec jekyll serve --livereload --drafts

# Build for production
bundle exec jekyll build

# Access at: http://localhost:4000
```

### Alternative: GitHub Pages

The site automatically builds and deploys when pushed to GitHub Pages without any additional configuration.

## Content Management

### Data-Driven Content

All structured content is managed through YAML files in `_data/`:

**Navigation Updates:**

- Edit `_data/navigation.yml` to modify site navigation
- Changes automatically apply to all pages

**Team Management:**

- Update `_data/team.yml` to add/modify organizers and volunteers
- Include social media links, images, and contact information

**Sponsor Management:**

- Edit `_data/sponsors.yml` to add new sponsors or partners
- Logos automatically display with proper linking

**Schedule Updates:**

- Modify `_data/schedule.yml` to update event timeline
- Changes reflect immediately on the homepage

### Adding New Site Locations

1. Create new Markdown file in `_sites/` directory (e.g., `_sites/new-city.md`)
2. Use the `site-location` layout
3. Add frontmatter with title, description, and keywords
4. Content automatically gets proper navigation and styling

### Page Creation

- **Standard Pages**: Create `.md` files in root with `layout: page`
- **Homepage**: Modify `index.md` with `layout: home`
- **Custom Layouts**: Extend `_layouts/` for specialized page types

### Content Updates

- **Event Information**: Update `_config.yml` for global event data
- **Registration Links**: Modify `_config.yml` links section
- **SEO Settings**: Update meta information in page frontmatter

## Navigation Structure

- Fixed navigation bar with responsive hamburger menu
- Consistent navigation across all pages
- External links: Registration (lu.ma) and Slack community

## Key Features

- **Countdown Timer**: JavaScript-powered countdown to event date
- **Responsive Design**: Works on all device sizes
- **FAQ Accordion**: Interactive expandable FAQ section
- **Loading Animation**: Smooth page load experience
- **Consistent Branding**: Blue gradient theme throughout

## Important URLs

- Registration (2026 edition): https://luma.com/ku88xh92
- Registration (2025, archived — hardcoded in historical `sites/*.html`): https://lu.ma/hspoki8y
- Slack Community: https://cutt.ly/llmhackathon-slack
- Contact: blaiszik@uchicago.edu

## Git Workflow

- Main branch: `main`
- Current working branch: `bb-aug12`
- No automated deployment - likely uses GitHub Pages or similar static hosting
