# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll-based charity fundraising website for Boatyardx Team Christmas Charity, hosted on GitHub Pages. The site features a countdown timer and live donation tracking that fetches data from a Google Sheets CSV export.

## Development Commands

### Local Development
```bash
bundle install                # Install Ruby gems
bundle exec jekyll serve      # Start local development server
```

The site will be available at `http://localhost:4000`. Note: Changes to `_config.yml` require restarting the server.

### Build
```bash
bundle exec jekyll build      # Build site to _site/ directory
```

## Architecture

### Jekyll Configuration
- **Theme**: minimal-mistakes-jekyll with "neon" skin
- **Content**: Single-page site with markdown files in root directory
- **Configuration**: `_config.yml` controls site settings, defaults, and theme customization
- **Built site**: Lives in `_site/` directory (excluded from git)

### Key Components

**index.markdown**: Main landing page with:
- Romanian language content for charity campaign
- JavaScript that fetches donation data from Google Sheets CSV
- Countdown timer to donation deadline (December 20, 2025)
- Auto-refreshing donation total (updates every 10 seconds)

**_config.yml**: Site configuration including:
- Theme and skin settings
- Site metadata (name, url, logo)
- Default layouts for pages and posts
- Footer content
- File inclusion/exclusion rules

**_data/navigation.yml**: Navigation menu structure (currently links to Boatyardx main site)

### GitHub Pages Deployment

The site uses GitHub Actions for automated deployment (`.github/workflows/jekyll.yml`):
- Triggers on pushes to master branch
- Builds with Ruby 3.2 and bundler cache
- Deploys to GitHub Pages automatically

The site is hosted at: `https://charity.boatyardx.com`

### Content Structure

- Root markdown files (*.markdown) become pages
- `_data/` contains YAML data files for navigation and other structured data
- `assets/` contains CSS, fonts, and images
- No `_posts/` or `_pages/` currently in use (empty)

### Custom Features

The main page includes custom JavaScript that:
1. Fetches CSV data from Google Sheets at regular intervals
2. Parses the first cell value as the current donation amount
3. Displays dynamic content showing how much Boatyardx has contributed
4. Shows countdown timer with red styling when less than 1 day remains

When working with the donation tracking, note that the CSV URL is hardcoded in index.markdown and uses cache-busting with `cache: "no-cache"`.
