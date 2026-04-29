# anuragkashyap.github.io

Personal site built with Jekyll. Auto-deploys via GitHub Pages.

## Local development

```bash
bundle install
bundle exec jekyll serve
```

Open http://localhost:4000

## Adding content

**A blog post:** new file in `_posts/YYYY-MM-DD-title.md`:
```yaml
---
title: "Post title"
date: 2026-04-29
tags: [ml, notes]
---
Post body in markdown.
```

**A project:** new file in `_projects/slug.md`:
```yaml
---
title: "Project name"
date: 2026-04-29
description: "One-line summary."
tags: [pytorch, rl]
github: "https://github.com/..."
demo: "https://..."
---
Long-form description.
```

**A publication:** new file in `_publications/slug.md`:
```yaml
---
title: "Paper title"
authors: "A. Kashyap, et al."
venue: "Venue, year"
year: 2026
arxiv: "https://arxiv.org/abs/..."
code: "https://github.com/..."
---
Optional notes.
```

## Customizing

- Site identity, links: `_config.yml`
- Colors, fonts, spacing: `assets/css/main.css` (CSS variables at the top)
- Layouts: `_layouts/`

## Deploy

Push to `main`. GitHub Pages picks it up automatically. Make sure the repo is named exactly `anuragkashyap.github.io` and Pages is enabled in repo settings.
