# harshakmohan.github.io

My personal site. Plain Jekyll, built automatically by GitHub Pages.

## Write a post

```bash
./new "My post title"
```

That creates `_posts/YYYY-MM-DD-my-post-title.md`. Write in Markdown below the `---` lines, then commit and push. It's live in about a minute.

No terminal handy? On GitHub, open `_posts/`, click **Add file → Create new file**, name it `2026-11-04-my-title.md`, and start with:

```markdown
---
title: My post title
---
```

**Drafts:** put unfinished posts in `_drafts/` (no date in the filename). They're never published. Preview them locally with `--drafts`.

**Editing:** just edit the file. Changing the date in the filename changes the post's date.

## Where things live

| File | What it does |
| --- | --- |
| `_config.yml` | Site title, description, footer links |
| `index.md` | Home page intro + post list |
| `style.css` | All styling. Fonts and colors are variables at the top |
| `_layouts/` | Page structure (rarely needs changes) |
| `_posts/` | Your articles |

Images: put them in `images/` and use `![alt text](/images/photo.jpg)`.

## Preview locally

```bash
bundle install
bundle exec jekyll serve --livereload --drafts
```

Then open http://localhost:4000.
