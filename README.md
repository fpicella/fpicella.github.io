# fpicella.github.io

Personal academic website of Francesco Picella. Plain HTML + CSS, no build step, served by GitHub Pages.

## Editing
- `index.html` — everything is in one page: about, news, research, publications, teaching, contact.
  - Add a news item: copy an `<li>` in `<ul class="news">`.
  - Add a paper: copy an `<li>` in `<ol class="pubs">` (newest first).
- `assets/style.css` — styles. Palette: set `data-palette="ink|slate|sepia"` on `<html>` in `index.html` (default: ink).
- `assets/photo.jpg` — portrait (square, ≥ 400 px). `assets/gmc2026.gif` — conference image shown in News.
- `cv/` — CV page; drop `cv-picella.pdf` there.
- Update `lastmod` in `sitemap.xml` and the footer date when you change content.

## Custom domain
Put the domain (e.g. `francescopicella.fr`) in a `CNAME` file at the root, then at the registrar add
`A` records → 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153 and `CNAME www → fpicella.github.io`.
Replace `https://fpicella.github.io/` by the domain in `index.html` (canonical, og:url, JSON-LD), `cv/index.html`, `robots.txt`, `sitemap.xml`.
