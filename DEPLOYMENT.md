# LLM Hackathon Website - Deployment Instructions

This guide covers how to install dependencies, run the site locally, and deploy to GitHub Pages.

## Prerequisites

- **Git** - Version control
- **Ruby** - Programming language (version 2.7.0 or higher)
- **Bundler** - Ruby dependency manager
- **GitHub account** with repository access

## 🛠️ Initial Setup

### 1. Install Ruby and Bundler

#### On macOS (using Homebrew)

```bash
# Install Homebrew if not already installed
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Install Ruby
brew install ruby

# Add Ruby to PATH (add to ~/.zshrc or ~/.bash_profile)
echo 'export PATH="/opt/homebrew/opt/ruby/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc

# Install Bundler
gem install bundler
```

#### On Ubuntu/Debian

```bash
# Update package list
sudo apt update

# Install Ruby and development tools
sudo apt install ruby-full build-essential zlib1g-dev

# Configure gem installation directory for user
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc

# Install Bundler
gem install bundler
```

#### On Windows

```bash
# Install Ruby using RubyInstaller
# Download from: https://rubyinstaller.org/downloads/
# Choose Ruby+Devkit version

# After installation, open command prompt and install Bundler
gem install bundler
```

### 2. Clone and Setup Repository

```bash
# Clone the repository
git clone https://github.com/llmhackathon/llmhackathon.github.io.git
cd llmhackathon.github.io

# Install Jekyll and dependencies
bundle install
```

## 🚀 Local Development

### Running the Site Locally

```bash
# Basic local server (rebuilds on file changes)
bundle exec jekyll serve

# With live reload (automatically refreshes browser)
bundle exec jekyll serve --livereload

# Include draft posts
bundle exec jekyll serve --drafts

# Serve on different port
bundle exec jekyll serve --port 4001

# Serve on all interfaces (accessible from other devices on network)
bundle exec jekyll serve --host 0.0.0.0
```

**Access the site at:** `http://localhost:4000`

### Development Workflow

1. **Make changes** to content files (`.md`), data files (`_data/*.yml`), or layouts
2. **Save files** - Jekyll automatically rebuilds the site
3. **Refresh browser** to see changes (automatic with `--livereload`)
4. **Commit changes** when ready to deploy

### Building for Production

```bash
# Build site for production (generates _site folder)
bundle exec jekyll build

# Build with production environment
JEKYLL_ENV=production bundle exec jekyll build
```

## 📤 GitHub Pages Deployment

### Automatic Deployment (Recommended)

GitHub Pages automatically builds and deploys Jekyll sites when you push to the repository.

```bash
# Add and commit your changes
git add .
git commit -m "Your commit message"

# Push to GitHub
git push origin main
```

**That's it!** GitHub Pages will automatically:

1. Detect the Jekyll site
2. Run `bundle exec jekyll build`
3. Deploy the built site
4. Make it available at your GitHub Pages URL

### Manual Deployment

If you prefer to build locally and deploy the generated files:

```bash
# Build the site
JEKYLL_ENV=production bundle exec jekyll build

# The built site is in the _site directory
# Commit and push the _site contents to gh-pages branch
git add _site
git commit -m "Deploy built site"
git subtree push --prefix _site origin gh-pages
```

## 🔧 Common Commands

### Content Management

```bash
# Add a new blog post
bundle exec jekyll post "Your Post Title"

# Add a new page
touch new-page.md
# Add frontmatter and content

# Check for broken links and other issues
bundle exec jekyll doctor
```

### Updating Dependencies

```bash
# Update all gems
bundle update

# Update specific gem
bundle update jekyll

# Check for outdated gems
bundle outdated
```

## 📝 Content Editing Guide

### Adding Navigation Items

Edit `_data/navigation.yml`:

```yaml
main:
  - name: "New Page"
    url: "/new-page.html"
```

### Adding Team Members

Edit `_data/team.yml`:

```yaml
volunteers:
  - name: "New Volunteer"
    image: "/assets/images/organizers/new-person.jpg"
    social:
      email: "person@example.com"
      github: "https://github.com/username"
```

### Adding Site Locations

Create `_sites/new-city.md`:

```yaml
---
layout: site-location
title: "New City"
description: "Details about the New City site"
---
## Welcome to New City Hub
Your content here...
```

### Updating Event Information

Edit `_config.yml`:

```yaml
event:
  dates: "September 11-12, 2025"
  countdown_date: "September 11, 2025 12:00:00"
```

## 🐛 Troubleshooting

### Common Issues

**Jekyll not found:**

```bash
# Ensure Ruby and Bundler are installed
ruby --version
bundler --version

# Reinstall if needed
gem install bundler jekyll
```

**Port already in use:**

```bash
# Use different port
bundle exec jekyll serve --port 4001

# Or kill process using port 4000
lsof -ti:4000 | xargs kill -9
```

**Permission errors:**

```bash
# On macOS/Linux, avoid using sudo with gem commands
# Instead, configure gem installation directory
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

**Build failures on GitHub Pages:**

- Check that all file names are lowercase
- Ensure no spaces in file names (use hyphens instead)
- Verify YAML frontmatter syntax
- Check GitHub Pages build logs in repository settings

### Debugging

```bash
# Verbose output
bundle exec jekyll serve --verbose

# Check site health
bundle exec jekyll doctor

# Build with detailed error messages
bundle exec jekyll build --trace
```

## 🌐 GitHub Pages Configuration

### Repository Settings

1. Go to repository **Settings** → **Pages**
2. **Source**: Deploy from a branch
3. **Branch**: `main` (or `gh-pages` if using manual deployment)
4. **Folder**: `/ (root)` (Jekyll sites use root, not `/docs`)

### Custom Domain (Optional)

If you have a custom domain:

1. Add `CNAME` file to repository root:

```
yourdomain.com
```

2. Configure DNS records:

```
Type: CNAME
Name: www
Value: yourusername.github.io
```

### HTTPS

GitHub Pages automatically provides HTTPS for `.github.io` domains and custom domains.

## 📊 Performance Optimization

### Image Optimization

```bash
# Install ImageMagick for image processing
brew install imagemagick  # macOS
sudo apt install imagemagick  # Ubuntu

# Optimize images
mogrify -resize 800x600 -quality 85 assets/images/*.jpg
```

### CSS Optimization

The site automatically minifies CSS in production mode when `JEKYLL_ENV=production`.

## 🔄 CI/CD (Advanced)

For automated testing and deployment, you can use GitHub Actions. Create `.github/workflows/jekyll.yml`:

```yaml
name: Build and Deploy Jekyll Site

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v3

      - name: Setup Ruby
        uses: ruby/setup-ruby@v1
        with:
          ruby-version: 3.0
          bundler-cache: true

      - name: Build site
        run: bundle exec jekyll build

      - name: Deploy to GitHub Pages
        if: github.ref == 'refs/heads/main'
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./_site
```

## 📞 Support

- **Jekyll Documentation**: https://jekyllrb.com/docs/
- **GitHub Pages Documentation**: https://docs.github.com/en/pages
- **Repository Issues**: Create an issue in the GitHub repository for site-specific problems
- **Community Support**: Join our [Slack community](https://cutt.ly/llmhackathon-slack)

---

**Quick Start Summary:**

1. `git clone [repository]`
2. `bundle install`
3. `bundle exec jekyll serve`
4. Make changes and push to GitHub for automatic deployment
