---
layout: post
title: "Dusk, December"
subtitle: "Light that stays just long enough."
date: 2026-04-16
category: Photo
---

Some introductory prose here. A few sentences to set the scene before the first gallery appears.

<!-- ═══════════════════════════════════════════
     ROW GALLERY — horizontal slider with captions
     Add is-16-9 or is-1-1 to each gallery__item.
     ═══════════════════════════════════════════ -->

<div class="gallery gallery--row">

  <div class="gallery__item is-16-9" data-src="{{ '/assets/images/photo-1.jpg' | relative_url }}">
    <img src="{{ '/assets/images/photo-1.jpg' | relative_url }}" alt="Crescent moon over rooftops" />
    <div class="gallery__caption-hidden">Crescent moon over rooftops, December 2025</div>
    <p class="gallery__caption">Crescent moon over rooftops, December 2025</p>
  </div>

  <div class="gallery__item is-1-1" data-src="{{ '/assets/images/photo-2.jpg' | relative_url }}">
    <img src="{{ '/assets/images/photo-2.jpg' | relative_url }}" alt="A square detail shot" />
    <div class="gallery__caption-hidden">A square detail shot</div>
    <p class="gallery__caption">A square detail shot</p>
  </div>

  <div class="gallery__item is-16-9" data-src="{{ '/assets/images/photo-3.jpg' | relative_url }}">
    <img src="{{ '/assets/images/photo-3.jpg' | relative_url }}" alt="Chimneys in silhouette" />
    <div class="gallery__caption-hidden">Chimneys in silhouette</div>
    <p class="gallery__caption">Chimneys in silhouette</p>
  </div>

</div>

More prose here between the two galleries.

<!-- ═══════════════════════════════════════════
     MASONRY GALLERY — grid, click to enlarge
     16:9 items span 2 columns automatically.
     1:1 items sit in a single column.
     ═══════════════════════════════════════════ -->

<div class="gallery gallery--masonry">

  <div class="gallery__item is-1-1" data-src="{{ '/assets/images/photo-4.jpg' | relative_url }}">
    <img src="{{ '/assets/images/photo-4.jpg' | relative_url }}" alt="Steam rising" />
    <div class="gallery__caption-hidden">Steam rising from a kettle at dawn</div>
  </div>

  <div class="gallery__item is-1-1" data-src="{{ '/assets/images/photo-5.jpg' | relative_url }}">
    <img src="{{ '/assets/images/photo-5.jpg' | relative_url }}" alt="Pineapple on a board" />
    <div class="gallery__caption-hidden">Pineapple on a cutting board</div>
  </div>

  <div class="gallery__item is-16-9" data-src="{{ '/assets/images/photo-6.jpg' | relative_url }}">
    <img src="{{ '/assets/images/photo-6.jpg' | relative_url }}" alt="Wide landscape shot" />
    <div class="gallery__caption-hidden">Wide landscape shot</div>
  </div>

  <div class="gallery__item is-1-1" data-src="{{ '/assets/images/photo-7.jpg' | relative_url }}">
    <img src="{{ '/assets/images/photo-7.jpg' | relative_url }}" alt="Detail" />
    <div class="gallery__caption-hidden">Detail</div>
  </div>

</div>

Closing prose to finish the post.
