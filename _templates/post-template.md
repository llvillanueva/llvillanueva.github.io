---
# ───────────────────────────────────────────────────────────────────────────
# COPY THIS FILE into _posts/ and rename it:  YYYY-MM-DD-short-title.md
#   e.g. _posts/2026-12-01-first-dive-of-winter.md
# The date in the file name is the publish date. Lines starting with # are notes;
# you can delete them.
# ───────────────────────────────────────────────────────────────────────────
layout: post
title: "Your post title"
date: 2026-12-01 10:00:00+0100
description: One sentence shown under the title on the .noise. page.
tags: [life]              # any of: research, freediving, films, photography, life (or new ones)
categories: []            # optional, e.g. [notes]
thumbnail:                # optional image shown in the list, e.g. assets/img/blog/my-photo.jpg
featured: false           # true pins the post as a card at the top of .noise.
toc:
  sidebar: false          # true adds a table of contents on the left for long posts
---

Write your opening paragraph here. Plain text is fine; Markdown adds formatting.

## A section heading

Some **bold**, some *italic*, and a [link](https://example.com).

- a bullet point
- another one

> A quote you liked.

### A photo

Put the image in `assets/img/blog/` and change the file name below.
{% include figure.html path="assets/img/blog/my-photo.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
<div class="caption">A caption for the photo.</div>

### Two photos side by side

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.html path="assets/img/blog/photo-1.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.html path="assets/img/blog/photo-2.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
  </div>
</div>

### Math (for research posts)

Inline: $$E = mc^2$$. On its own line:

$$
\frac{\partial \theta}{\partial t} + \mathbf{u}\cdot\nabla\theta = 0
$$

### Code

```python
import xarray as xr
ds = xr.open_dataset("radiosonde.nc")
```
