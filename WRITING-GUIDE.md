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

```html
<div class="single-image">
  <div class="gallery__item" data-src="{{ '/assets/images/photo.jpg' | relative_url }}">
    <img src="{{ '/assets/images/photo.jpg' | relative_url }}" alt="Describe the photo" />
    <div class="gallery__caption-hidden">Caption shown in lightbox</div>
    <p class="gallery__caption">Caption shown below the photo</p>
  </div>
</div>
```

- Both captions can be the same text, or the lightbox version can be longer
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

  <div class="gallery__item" data-src="{{ '/assets/images/photo.jpg' | relative_url }}">
    <img src="{{ '/assets/images/photo.jpg' | relative_url }}" alt="Describe the photo" />
    <div class="gallery__caption-hidden">Caption shown in lightbox</div>
    <p class="gallery__caption">Caption shown below the thumbnail</p>
  </div>

</div>
```

- The `<p class="gallery__caption">` appears **below** the photo in the slider
- The `<div class="gallery__caption-hidden">` appears **in the lightbox** when clicked
- They can be the same text or different

---

## Adding a MASONRY gallery (grid, click to enlarge)

```html
<div class="gallery gallery--masonry">

  <div class="gallery__item" data-src="{{ '/assets/images/photo.jpg' | relative_url }}">
    <img src="{{ '/assets/images/photo.jpg' | relative_url }}" alt="Describe the photo" />
    <div class="gallery__caption-hidden">Caption shown in lightbox</div>
  </div>

</div>
```

- No visible caption on the grid — captions appear only in the lightbox
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
