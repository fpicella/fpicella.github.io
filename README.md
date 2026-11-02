# fpicella.github.io

Personal website of Francesco Picella. One page, plain HTML + CSS, no build step, served by GitHub Pages.

## Where things go
| What | Where |
|---|---|
| Portrait (square, ≥ 600 px) | `assets/img/portrait.jpg` |
| Lab / university logo (optional, shown next to the affiliation) | `assets/img/logo-dalembert.png` |
| Research figures (4) | `assets/img/research-*.png` (names in `index.html`) |
| Publication thumbnails | `assets/pubs/<year>-<journal>.png` (names in `index.html`) |
| News / gallery photos, gifs, videos | `assets/media/` |
| CV | `assets/cv-picella.pdf` |
| Internship offers | `assets/stages/*.pdf` |

Until a picture exists, its slot shows a striped "image to add" box; drop the file in and it appears.

## Editing `index.html`
- **News**: copy one `<li class="news-item">`. A news item may carry a `<figure class="media">` with an image, a gif, a local video (`<video controls>` + `.mp4`) or a YouTube embed (`<div class="yt"><iframe src="https://www.youtube-nocookie.com/embed/VIDEO_ID" …></iframe></div>`).
- **Research**: one `<article class="row">` per topic (figure + text; rows alternate sides automatically).
- **Publications**: one `<article class="pub">` per paper — thumbnail, linked title, one-line summary, citation with `<b>Picella F.</b>`.
- **Talks & media**: one `<figure class="card">` per item (photo, video or YouTube).
- Keep `<title>`, meta description and the JSON-LD block up to date (name, URL, links) — that is what Google reads.
- When content changes, update `lastmod` in `sitemap.xml`.

## Custom domain
Create a file `CNAME` at the root containing the domain (e.g. `francescopicella.com`). At the registrar add
`A` records → 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153 and `CNAME www → fpicella.github.io`.
Then replace `https://fpicella.github.io/` by the domain in `index.html` (canonical, og:url, JSON-LD), `robots.txt` and `sitemap.xml`, and tick "Enforce HTTPS" in the repo settings → Pages.
