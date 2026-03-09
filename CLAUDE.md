# CLAUDE.md — Project Guide for Claude Code

## Project Overview

This is **Saani Rawat's personal academic website**, hosted on GitHub Pages at [saannidhya.github.io](https://saannidhya.github.io). It is built with **Jekyll** using the [AcademicPages](https://github.com/academicpages/academicpages.github.io) template (a fork of Minimal Mistakes).

## Tech Stack

- **Static Site Generator:** Jekyll (Ruby)
- **Templating:** Liquid templates + Kramdown Markdown
- **Styling:** SCSS (in `_sass/`)
- **Hosting:** GitHub Pages (auto-builds on push to `master`)
- **Theme:** AcademicPages / Minimal Mistakes

## Repository Structure

```
_config.yml          # Site-wide settings (title, author, collections, plugins)
_data/
  navigation.yml     # Header nav links
  cv.json            # Structured CV data
_pages/              # Top-level site pages (about, research, cv, teaching, etc.)
_publications/       # Individual publication entries (Markdown + front matter)
_teaching/           # Teaching entries
_talks/              # Talk entries
_posts/              # Blog posts (if used)
_portfolio/          # Portfolio entries
_layouts/            # Page layout templates (HTML + Liquid)
_includes/           # Reusable HTML partials (author-profile, head, footer, etc.)
_sass/               # SCSS stylesheets
assets/              # Static assets (JS, CSS, images)
images/              # Site images (avatar, etc.)
files/               # Downloadable files (CV PDF, papers, etc.)
```

## Key Pages & Navigation

Navigation is controlled by `_data/navigation.yml`. Current active pages:
- **About** (`/`) — `_pages/about.md`
- **Research** (`/research/`) — `_pages/research.md`
- **Teaching** (`/teaching/`) — `_pages/teaching.html`
- **CV** — links to `files/Saani_Rawat_CV.pdf`

## Content Conventions

- Page content uses inline HTML `<span style="font-size:.9em;">` for text sizing
- Research entries are hand-written in `_pages/research.md` (not using the `_publications` collection for display)
- The `_publications/` collection exists but is not linked in navigation
- Front matter follows Jekyll standards (`layout`, `permalink`, `title`, `author_profile`)

## Development

### Local Preview
```bash
bundle install
bundle exec jekyll serve
```
Or via Docker:
```bash
docker-compose up
```

### Deployment
Push to `master` branch — GitHub Pages builds automatically.

## Editing Guidelines

- **Do not break existing page layouts or navigation** without confirming with the user
- Keep inline styling consistent with existing patterns (font-size: .9em for body text)
- PDFs and downloadable files go in `files/`
- Images go in `images/`
- When updating research content, edit `_pages/research.md` directly
- When updating the about page, edit `_pages/about.md`
- Always test Markdown/HTML changes for proper rendering before committing
