# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **Jekyll-powered static website** for the **LLM Hackathon for Applications in Materials Science & Chemistry** - an international hybrid hackathon event. The website serves as the main information hub for participants, organizers, and site hosts.

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

- **CSS Framework**: Uses Tailwind CSS (via CDN) + custom CSS
- **Typography**: Poppins (primary) and Roboto Mono (monospace) fonts from Google Fonts
- **Responsive Design**: Mobile-first approach with breakpoints for tablets and desktop
- **Color Scheme**: Blue gradient theme (`#027ff7` to `#0259ce`) with clean white/gray backgrounds
- **Components**: Reusable card layouts for projects, resources, team members, and prizes

## Development Commands

### Jekyll Development

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

- Registration: https://lu.ma/hspoki8y
- Slack Community: https://cutt.ly/llmhackathon-slack
- Contact: blaiszik@uchicago.edu

## Git Workflow

- Main branch: `main`
- Current working branch: `bb-aug12`
- No automated deployment - likely uses GitHub Pages or similar static hosting
