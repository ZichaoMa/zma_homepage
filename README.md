# zma_homepage

Zichao Ma's academic homepage. Built on [Academic Pages](https://github.com/academicpages/academicpages.github.io) (a fork of [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/)), hosted via GitHub Pages.

Live at: https://katorid.github.io/zma_homepage/

## Editing content

- `_config.yml` — site-wide settings: name, bio, links, social profiles.
- `_pages/about.md` — front page / bio.
- `_pages/cv.md` — education, positions, service (publications/talks/teaching sections pull automatically from the collections below).
- `_publications/`, `_talks/`, `_teaching/`, `_portfolio/` — one Markdown file per item. See `markdown_generator/` for scripts that convert a spreadsheet or BibTeX file into these Markdown files in bulk.
- `images/profile.png` — replace with your own photo (keep the filename, or update `author.avatar` in `_config.yml`).

## Publishing

GitHub Pages builds automatically from the `master` branch (Settings → Pages → Source: Deploy from a branch → master / root). No CI/build step required — GitHub's built-in Jekyll builder handles it.
