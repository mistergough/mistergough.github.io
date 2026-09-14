# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Personal portfolio and blog site (mistergough.com) built with Jekyll 3.9.3 (pinned via the `github-pages` gem) and deployed via GitHub Pages. Styles are in a single SASS file; photo galleries use Lightbox Plus jQuery.

## Commands

```bash
bundle install
bundle exec jekyll serve   # http://localhost:4000
bundle exec jekyll build
```

## Content

- **_posts/** — Blog articles (`.md` or `.html`). Older posts carry verbose WordPress-era front matter (categories, tags, meta arrays) that is vestigial but harmless.
- **Root `.md` files** — Individual pages (`index.md`, `teaching.md`, `portfolio.md`, `thanks.md`) plus photo set pages (`nature.md`, `street.md`, `architecture.md`).
- **`blog.html`** — Paginated post archive (`paginate: 1` in `_config.yml`).
- **`photos.html`** — Index linking to individual photo set pages.

## Photo Galleries

Photo set pages use `layout: photo_set` with this front matter pattern:

```yaml
photos:
  set: nature
  size: 6
```

The layout loops from `1` to `photos.size`, loading `/images/<set>/1.jpg`, `2.jpg`, etc. To add a new gallery, create a root `.md` page with this pattern and place sequentially numbered images in `/images/<set-name>/`.

## Layouts and Includes

- `_layouts/post.html` — Includes custom Liquid date formatting (ordinals: "1st", "2nd") and Disqus comments.
- `_layouts/page.html` — Supports optional `image:` front matter for a featured image; also includes Disqus.
- `_includes/footer.html` — Email address is JavaScript-obfuscated.
- `_includes/form.html` — Formspree contact form; redirects to `/thanks` on submission.

## Deployment

Push to `master` on GitHub (`mistergough/mistergough.github.io`) to trigger an automatic GitHub Pages build and deploy.
