# How to write a post

## Creating a new post

1. Create a new file in the `_posts/` folder
2. Name it: `YYYY-MM-DD-your-title.md`
3. Start with front matter (see below)
4. Write your post underneath
5. Commit and push — GitHub builds it automatically

---

## Front matter

```
---
layout: post
title: "Your title here"
subtitle: "An optional one-liner."
date: 2026-04-20
category: Note
---
```

**Category options (use anything you like):** Note · Photo · Essay · Field

---

## Writing in Markdown

```
## Section heading        (Comfortaa, large)
### Smaller heading       (Alegreya Sans)

*italic*    **bold**

> Blockquote or pulled quote

[link text](https://example.com)
```

---

## Adding a single photo

Use the `single-image` class for one photo sitting within the text column (68ch wide). The caption appears below the photo on the page and also in the lightbox when clicked.
Note that Lightbox caption styling is defined in gallery.css by ".lg-sub-html"

```html
<div class="single-image">
  <div
    class="gallery__item"
    data-src="{{ '/assets/images/photo.jpg' | relative_url }}"
    data-sub-html="Caption shown in lightbox"
  >
    <img
      src="{{ '/assets/images/photo.jpg' | relative_url }}"
      alt="Brief description for screen readers"
    />
    <p class="gallery__caption">Caption shown below the photo</p>
  </div>
</div>
```

- `data-sub-html` — the caption shown in the lightbox overlay when the photo is clicked
- `alt` — a brief description for screen readers and broken-image fallback; not shown visually
- `gallery__caption` — the caption shown below the photo on the page
- The photo displays at its natural ratio — no cropping
- Use this for a single feature photo within a text-heavy post

For a plain inline photo with no lightbox or caption:

```
![Alt text]({{ '/assets/images/your-photo.jpg' | relative_url }})
```

---

## Adding a ROW gallery (slider with captions)

Paste this block wherever you want the slider to appear in your post.
Duplicate the `gallery__item` block for each photo.

```html
<div class="gallery gallery--row">
  <div
    class="gallery__item is-16-9"
    data-src="{{ '/assets/images/photo.jpg' | relative_url }}"
    data-sub-html="Caption shown in lightbox"
  >
    <img
      src="{{ '/assets/images/photo.jpg' | relative_url }}"
      alt="Brief description for screen readers"
    />
    <p class="gallery__caption">Caption shown below the thumbnail</p>
  </div>
</div>
```

- `data-sub-html` — caption shown in the lightbox when clicked
- `gallery__caption` — caption shown below the photo in the slider
- They can be the same text or different
- Add `is-16-9` or `is-1-1` to the `gallery__item` div to match your photo's ratio

---

## Adding a MASONRY gallery (grid, click to enlarge)

```html
<div class="gallery gallery--masonry">
  <div
    class="gallery__item is-1-1"
    data-src="{{ '/assets/images/photo.jpg' | relative_url }}"
    data-sub-html="Caption shown in lightbox"
  >
    <img
      src="{{ '/assets/images/photo.jpg' | relative_url }}"
      alt="Brief description for screen readers"
    />
  </div>
</div>
```

- `data-sub-html` — caption shown in the lightbox when clicked
- No visible caption on the grid — captions appear only in the lightbox
- Add `is-16-9` or `is-1-1` to match your photo's ratio
- Photos sit at their natural aspect ratio, so portrait and landscape mix naturally

---

## Image prep

Resize photos to ~200KB before committing.

**Mac terminal (one photo):**

```
sips -Z 1600 your-photo.jpg
```

**Mac terminal (whole folder):**

```
for f in *.jpg; do sips -Z 1600 "$f"; done
```

**Online:** https://squoosh.app

Put all images in `assets/images/` in your repo.

---

## Post URL structure

`https://yhlreporter.github.io/site/CATEGORY/YYYYMMDD/your-title/`
