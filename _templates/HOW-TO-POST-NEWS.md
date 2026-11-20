# How to post news

News shows on the homepage (**.source.**) under **NEWS**, newest first.
The homepage shows the 5 most recent items; all of them are listed at `/news/`.

## 1. Create the news item
1. Copy `_templates/news-template.md` into `_news/`.
2. Rename it to `YYYY-MM-DD-short-name.md`
   (e.g. `_news/2026-12-01-agu-poster.md`). Lowercase, dashes, no spaces.
3. Set the `date:` line to the same date.
4. Replace the example sentence with your news.

That's it. A short news item is just this:

```markdown
---
layout: post
date: 2026-12-01
inline: true
related_posts: false
---

Presenting a poster on multilayer clouds at [AGU 2026](https://www.agu.org/annual-meeting) in San Francisco 🪧
```

## 2. Short vs. long news
| | `inline: true` (default) | `inline: false` |
|---|---|---|
| Homepage shows | the whole text | only the `title:`, as a link |
| Use for | one or two sentences | a longer story with photos |

For a long one, set `inline: false`, add a `title: "..."`, and write as much as you like below
the second `---` (photos work the same way as in blog posts; see `HOW-TO-POST.md`).

## 3. Writing tips
- **Link:** `[text](https://...)`; **italic title:** `[*Paper title*](https://doi.org/...)`
- **Link to your own pages:** `[my poster](/repositories/#posters)`, `[CV](/cv/)`, `[.noise. post](/blog/2026/post-name/)`
- **Emoji:** paste them directly 🎉, or write `:tada:`
- Keep it to one or two lines so the homepage stays tidy.

## 4. Often goes together with…
- **New paper or preprint** → also add it to `_bibliography/papers.bib` (shows on **.sink.**).
- **Conference, school, workshop** → also add it to `_data/research.yml` (shows on **.sink.** and the CV).
- **Poster** → also add it to `_data/posters.yml` and put the PDF in `assets/pdf/`.

## 5. Preview and publish
- Preview: `docker compose up`, then open http://localhost:8080
- Publish (from `dev`):
  ```bash
  git add -A && git commit -m "News: short description"
  git checkout master && git merge dev && git push origin master
  git checkout dev
  ```

## Remove or edit news
Edit the file in `_news/` or delete it; the homepage updates on the next build.

## Settings
In `_config.yml` under `announcements:`
- `limit: 5`: how many items show on the homepage
- `scrollable: true`: adds a scroll bar when there are more than 3
