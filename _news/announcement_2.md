---
layout: post
title: How to post news on this site
date: 2026-03-13 08:00:00+0100
inline: false
related_posts: false
---

News items on this site live in the `_news/` folder. Each item is a Markdown file with a small YAML front-matter block at the top. Here is a quick guide.

---

### Short (inline) announcement

Create a file like `_news/announcement_N.md` with the following front matter:

```yaml
---
layout: post
date: YYYY-MM-DD HH:MM:SS±HHMM
inline: true
related_posts: false
---

Your short announcement text here.
```

Inline items appear as a single line in the *News* section of the home page.

---

### Long announcement (with its own page)

Set `inline: false` and add a `title`:

```yaml
---
layout: post
title: My announcement title
date: YYYY-MM-DD HH:MM:SS±HHMM
inline: false
related_posts: false
---

Full Markdown content goes here. You can use **bold**, _italic_, lists, images, code blocks, and more.
```

Long announcements get their own page that visitors can navigate to.

---

### Tips

- File names can be anything; a good convention is `announcement_N.md` or a short slug like `my-event.md`.
- The `date` field controls the order in which news items are listed (newest first).
- Markdown, HTML, emoji `:sparkles:`, and LaTeX math are all supported.
- The home page shows the most recent **{{ site.announcements.limit }}** items (configured via `announcements.limit` in `_config.yml`).

