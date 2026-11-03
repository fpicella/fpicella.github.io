# fpicella.github.io

Personal website of Francesco Picella. Plain HTML + CSS, no build step, served by GitHub Pages at https://francescopicella.com.

## Pages
| File | Page |
|---|---|
| `index.html` | Home: hero, research teasers, the three latest news, join, contact |
| `research.html` | Research: Bioconvection, Artificial active matter, Underwater superhydrophobic surfaces (TARAS), Stability of coupled flows, Tools in Basilisk |
| `publications.html` | Publications (one `<article class="pub">` per paper; anchors like `#jfm2022` are linked from the research page) |
| `news.html` | All news, newest first (copy the three most recent to `index.html`) |
| `talks.html` | Talks, videos, pictures from the road |
| `teaching.html` | Courses |
| `positions.html` | Internship offers and former students (with their Basilisk sandboxes) |

The header and the nav are repeated at the top of every page: when adding a page, copy them and move `aria-current="page"` to the new link.

## Where things go
| What | Where |
|---|---|
| Portrait (square, ≥ 600 px) | `assets/img/portrait.jpg` |
| Lab / university logo (optional, shown next to the affiliation) | `assets/img/logo-dalembert.png` |
| Project figures, posters of the videos | `assets/img/` |
| Project videos (mp4, H.264, ≤ ~3 MB each) | `assets/media/` |
| Publication thumbnails | `assets/pubs/<year>-<journal>.png` (names in `publications.html`) |
| News / gallery photos, gifs, videos | `assets/media/` |
| CV | `assets/cv-picella.pdf` |
| Internship offers | `assets/stages/*.pdf` |

Until a picture exists, its slot shows a striped "image to add" box; drop the file in and it appears.

## Editing
- **News**: copy one `<li class="news-item">`. A news item may carry a `<figure class="media">` with an image, a gif, a local video (`<video controls>` + `.mp4`) or a YouTube embed (`<div class="yt"><iframe src="https://www.youtube-nocookie.com/embed/VIDEO_ID" …></iframe></div>`).
- **Research**: one `<article class="project">` per project (text left, figure right, optional full-width `<figure class="fig wide film">` with a video); end each with a `<p class="collab">` line naming the collaborators.
- **Publications**: one `<article class="pub">` per paper — thumbnail, linked title, one-line summary, citation with `<b>Picella F.</b>`.
- **Talks & media**: one `<figure class="card">` per item (photo, video or YouTube).
- Keep `<title>`, meta description and the JSON-LD block up to date (name, URL, links) — that is what Google reads.
- When content changes, update `lastmod` of that page in `sitemap.xml`.

## Custom domain
Create a file `CNAME` at the root containing the domain (e.g. `francescopicella.com`). At the registrar add
`A` records → 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153 and `CNAME www → fpicella.github.io`.
Then replace `https://fpicella.github.io/` by the domain in `index.html` (canonical, og:url, JSON-LD), `robots.txt` and `sitemap.xml`, and tick "Enforce HTTPS" in the repo settings → Pages.
