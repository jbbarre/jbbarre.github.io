# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

Personal academic/portfolio website for Jean Baptiste Barré, built with the [al-folio](https://github.com/alshedivat/al-folio) Jekyll theme. Deployed to GitHub Pages from the `master` branch.

## Development commands

**Local dev with Docker (recommended):**
```bash
# Using prebuilt DockerHub image
docker compose up

# Using locally built image (Dockerfile)
docker compose -f docker-local.yml up
```
The site runs at http://localhost:8080 with live reload.

**Native Jekyll (requires Ruby + bundler):**
```bash
bundle install
bundle exec jekyll serve --watch --port=8080 --livereload
```

**Build for production:**
```bash
bundle exec jekyll build   # or: bin/cibuild
```

**Deploy to gh-pages branch:**
```bash
bin/deploy   # prompts for confirmation, requires clean working tree
```

## Content structure

Content lives in these directories — no build step needed, just edit the Markdown/YAML:

| Directory | Purpose |
|-----------|---------|
| `_pages/` | Top-level pages (about, cv, projects, publications, etc.) |
| `_news/` | News/announcements (short Markdown files) |
| `_projects/` | Project cards shown on the projects page |
| `_posts/` | Blog posts |
| `_data/cv.yml` | CV content rendered by `_layouts/cv.html` — structured as `title/type/contents` entries |
| `_data/repositories.yml` | GitHub repos shown on the repositories page |
| `_data/coauthors.yml` | Co-author link mapping for publications |
| `_bibliography/papers.bib` | BibTeX bibliography for the publications page (processed by jekyll-scholar) |

## Architecture

- **`_config.yml`** is the central config file — site identity, feature flags (`enable_*`), plugin settings, and CDN library versions all live here.
- **`_layouts/`** defines page templates; `default.html` wraps everything, `cv.html` iterates `_data/cv.yml`.
- **`_includes/`** holds reusable partials (head, header, footer, social links, scripts).
- **`_sass/`** contains theme styles; `_variables.scss` and `_themes.scss` control light/dark mode colors.
- **`assets/img/`** images are auto-converted to WebP at multiple resolutions by `jekyll-imagemagick` on build.
- The publications page uses `jekyll-scholar` — bibliography is sourced from `_bibliography/papers.bib`.
- Dark mode, math (MathJax), masonry layout, and medium-zoom are optional features toggled in `_config.yml` under `enable_*` keys.
