# How to write a post

## Creating a new post

1. Create a new file in the `_posts/` folder
2. Name it exactly like this: `YYYY-MM-DD-your-title.md`
   - Example: `2026-04-20-notes-on-the-monsoon.md`
3. Start the file with a front matter block (see below)
4. Write your post underneath it
5. Commit and push — GitHub builds it automatically

---

## Front matter

Every post must start with this block between the triple dashes:

```
---
layout: post
title: "Your title here"
subtitle: "An optional one-liner."
date: 2026-04-20
category: Note
---
```

**Fields:**
- `title` — required. Shown as the big heading.
- `subtitle` — optional. Shown in smaller italic text below the title.
- `date` — required. Format: YYYY-MM-DD.
- `category` — optional. Shown next to the date. Use whatever label fits: Note, Photo, Essay, Field, etc.

---

## Writing in Markdown

### Paragraphs
Just write. A blank line between paragraphs creates a new paragraph.

### Headings
```
## Section heading       (Comfortaa, large)
### Smaller heading      (Alegreya Sans, medium)
```

### Emphasis
```
*italic*
**bold**
```

### Blockquote
```
> This is a pulled quote or a citation.
```

### Links
```
[link text](https://example.com)
```

### Images
```
![Alt text](../assets/images/your-photo.jpg)
```
Put your photos in `assets/images/` before adding them to a post.
Resize photos to ~200KB before committing (see image guide below).

### Photo galleries
Phase 5 will add gallery support. For now, add photos one by one using the image syntax above.

---

## Image sizing guide

Before adding a photo to your repo, resize it to roughly 200KB.

**On Mac, using the terminal (one photo):**
```
sips -Z 1600 your-photo.jpg
```

**On Mac, resize a whole folder at once:**
```
for f in *.jpg; do sips -Z 1600 "$f"; done
```

**On Windows:**
Use Paint or Photos app → Resize → set width to 1600px.

**Online:**
https://squoosh.app — drag, resize, download. Free and excellent.

---

## Post URL structure

Your posts will be available at:
`https://yhlreporter.github.io/CATEGORY/YYYY/MM/DD/your-title/`

Example:
`https://yhlreporter.github.io/note/2026/04/20/notes-on-the-monsoon/`
