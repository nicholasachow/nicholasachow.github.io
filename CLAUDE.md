# nicholasachow.com

Jekyll site using a heavily stripped-down Beautiful Jekyll theme.

## Stack
- No jQuery, Bootstrap JS, or Font Awesome — pure CSS only
- Only external dependency: Google Fonts (Poppins)
- Build: `bundle exec jekyll build`

## Architecture
- `assets/css/custom-styles.css` — all custom styling; overrides everything in beautifuljekyll.css
- `assets/css/beautifuljekyll.css` — stripped base theme CSS; don't re-add removed features (search, social share, avatars, dropdowns, big-img headers)
- `_layouts/base.html` — root layout; only loads Google Fonts externally
- No comments, analytics, or social sharing enabled

## Design
- Minimal, vaughntan.org-inspired aesthetic
- Blue links (#0000FF), white background, Poppins font throughout
- Static navbar (not fixed), left-aligned content column

## Content
- Posts in `_posts/` are metadata-only stubs: `title`, optional `subtitle`, and `external_url` — no body content
- They render via `_layouts/redirect.html`, which keeps the old permalink alive and redirects to the canonical Substack post
- Blog listing (`_layouts/home.html`) links each entry straight out to its `external_url`
