# Lloyd Villanueva — personal website

Source for [llvillanueva.github.io](https://llvillanueva.github.io/), built with Jekyll and the [al-folio](https://github.com/alshedivat/al-folio) theme (MIT license).

## Where things live

| What | File |
| --- | --- |
| Homepage text | `_pages/about.md` |
| CV page | `assets/json/resume.json` |
| Publications | `_bibliography/papers.bib` (`selected={true}` shows a paper on the homepage) |
| Repositories page | `_data/repositories.yml` |
| Site settings, social links | `_config.yml` |
| Profile photo | `assets/img/prof_pic.jpg` |

Optional, currently off:

- **News on the homepage:** add `.md` files to `_news/`, set `news: true` in `_pages/about.md`, and uncomment the `news` collection in `_config.yml`.
- **Blog:** add posts to `_posts/` and set `blog_nav_title` in `_config.yml`.
- **CV PDF download:** put the PDF in `assets/pdf/` and uncomment `cv_pdf` in `_pages/cv.md`.

## Run locally

```bash
docker compose up   # then open http://localhost:8080
```

Pushing to `master` builds and deploys the site through GitHub Actions.
