# How to post on .noise.

## 1. Create the post
1. Copy `_templates/post-template.md` into `_posts/`.
2. Rename it to `YYYY-MM-DD-short-title.md` (e.g. `2026-12-01-first-dive-of-winter.md`).
   Use lowercase and dashes; the date is the publish date.
3. Fill in the part between the two `---` lines:
   - `title`: the headline
   - `description`: one line shown on the .noise. page
   - `tags`: hashtags, e.g. `[freediving, photography]`
4. Write the post below the second `---`. Delete the example sections you don't need.

## 2. Add photos (optional)
- Put images in `assets/img/blog/`. JPGs under ~1 MB load fastest.
- Use them with the `figure.html` snippet in the template, or as the list thumbnail
  with `thumbnail: assets/img/blog/your-photo.jpg`.

## 3. Preview
Run `docker compose up` in the terminal and open http://localhost:8080/blog/
(save the file, then refresh the page).

## 4. Publish
In VS Code: Source Control → write a message (e.g. "New post: first dive of winter")
→ Commit → Sync/Push. The live site updates a few minutes later.

## Hashtags
The hashtags at the top of .noise. are set in `_config.yml` → `display_tags`.
A post can use any tag; only the ones listed there show up as filters at the top.
Each tag also gets its own page, e.g. /blog/tag/freediving/.

## Drafts
Not ready yet? Keep the file in `_drafts/` (no date in the file name). It won't be published.

## Show a post in the homepage news
(Full news guide: `_templates/HOW-TO-POST-NEWS.md`.)
Add a file to `_news/`, e.g. `_news/2026-12-01-new-post.md`:

    ---
    layout: post
    date: 2026-12-01
    inline: true
    ---
    New on .noise.: [First dive of winter](/blog/2026/first-dive-of-winter/) 🤿
