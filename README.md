# SIHINA 2026/2027 – Team Rad KDU

Single-page site: `index.html`.

## Folder layout

```
images/                 web-ready copies used by the site (max 1600px; hero 1920px)
  hero/01-05.jpg        hero background slideshow
  gallery/01-11.jpg     "Inside the project" gallery
  history/intake-NN/    photos for each intake in "SIHINA through the years"
  */thumb/              640px thumbnails for the photo grids
source/                 original uploads, renamed to match images/ (same numbers)
  descriptions/         intake write-ups (.docx)
```

The same images are on Cloudinary under `sihina/<same path>` (e.g. `sihina/history/intake-38/01`).
In `index.html`, `CDN` switches between Cloudinary and the local `images/` copies.

## Adding photos

1. Put the original in `source/<folder>/` with the next number (e.g. `12.jpg`).
2. Add a resized copy to `images/<folder>/` and a 640px copy to `images/<folder>/thumb/`.
3. Upload it to Cloudinary as `sihina/<folder>/12`.
4. Bump the count in `index.html` (e.g. `seq("gallery", 12)`).
