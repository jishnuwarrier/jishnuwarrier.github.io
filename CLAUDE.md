# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Architecture Overview

This is a Jekyll-based academic portfolio website. The site is a static site generator with the following key components:

- **Jekyll**: Static site generator configured via `_config.yml`
- **Ruby/Bundler**: Dependency management via `Gemfile`
- **Sass**: CSS preprocessing with files in `_sass/`
- **Liquid**: Templating engine used in layouts and includes
- **Docker**: Containerized development environment

### Key Directories

- `_pages/`: Main site pages (about, publications, projects, etc.)
- `_posts/`: Blog posts in Markdown format
- `_projects/`: Project showcase content
- `_layouts/`: HTML templates using Liquid
- `_includes/`: Reusable template components
- `_sass/`: Sass/SCSS stylesheets
- `_data/`: YAML data files (CV, repositories, etc.)
- `_plugins/`: Custom Jekyll plugins
- `assets/`: Static assets (images, PDFs, JSON data)

## Development Commands

### Local Development (Docker - Recommended)
```bash
# Pull and start development server
docker compose pull
docker compose up

# Alternative slim version
docker compose -f docker-compose-slim.yml up

# Build custom image
docker compose up --build
```

Site will be available at `http://localhost:8080`

### Local Development (Legacy)
```bash
# Install dependencies
bundle install
pip install jupyter

# Start Jekyll server
bundle exec jekyll serve
```

Site will be available at `http://localhost:4000`

### Build Commands
```bash
# Build site for production
bundle exec jekyll build

# CSS optimization (after build)
purgecss -c purgecss.config.js
```

### Code Quality
```bash
# Format code
npx prettier --write .

# Format with Liquid plugin for Jekyll templates
npx prettier --write . --plugin=@shopify/prettier-plugin-liquid
```

## Configuration Files

- `_config.yml`: Main Jekyll configuration
- `Gemfile`: Ruby dependencies and Jekyll plugins
- `package.json`: Node.js dependencies (Prettier)
- `purgecss.config.js`: CSS optimization configuration
- `docker-compose.yml`: Docker development setup

## Content Management

### Publications
- Bibliography managed in `_bibliography/papers.bib`
- Configured via `jekyll-scholar` plugin
- Display settings in `_config.yml` under `scholar` section

### Projects
- Individual project files in `_projects/` directory
- Uses Jekyll collections functionality

### CV/Resume
- Two formats supported: JSON (`assets/json/resume.json`) and YAML (`_data/cv.yml`)
- JSON format follows jsonresume.org standard
- YAML fallback for more readable editing

### Blog Posts
- Markdown files in `_posts/` directory
- Support for Distill-style posts with special layouts
- Categories and tags configured in frontmatter

## Deployment

The site auto-deploys to GitHub Pages when pushed to main branch via GitHub Actions (`.github/workflows/deploy.yml`). Manual deployment options include:

- GitHub Pages (recommended)
- Netlify
- Custom hosting (build locally with `bundle exec jekyll build`)

## Theme Customization

- Theme colors: `_sass/_themes.scss`
- Layout styles: `_sass/_layout.scss`
- Component styles: Individual files in `_sass/`
- Site configuration: `_config.yml`

## Key Features

- Responsive design with dark/light mode
- Mathematics support via MathJax
- Code syntax highlighting
- Image optimization and lazy loading
- Search functionality
- Social media integration
- Google Analytics and other analytics platforms