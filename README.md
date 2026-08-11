# Personal site — Kuma Lawrence

Portfolio and CV for **Kuma Lawrence**, a developer working in quantitative
research and data engineering, based in Cape Town.

**Live:** <https://kuma2018shing.github.io/CV/>

---

## About the build

A static, dependency-free single page. No framework, no build step, no
package manager — the deployed output is the source.

| | |
|---|---|
| Markup | Semantic HTML5 |
| Styling | Hand-written CSS, custom properties, grid and flexbox |
| Type | Inter (UI and body), JetBrains Mono (data and labels) |
| Hosting | GitHub Pages, served from `master` |
| JavaScript | ~15 lines: copyright year, nav scroll-spy |

### Design notes

- **Mobile-first.** Layout is fluid via `clamp()` rather than fixed
  breakpoints, so type and spacing scale continuously.
- **Dark by default**, with a full light theme through
  `prefers-color-scheme`.
- **Accessible.** Skip link, visible focus rings, semantic landmarks,
  decorative imagery marked `aria-hidden` with empty `alt`, and
  `prefers-reduced-motion` respected.
- **Light.** One image on the whole page; the hero chart is inline SVG, so
  it costs no extra request.

## Structure

```
.
├── index.html          # entire page
├── css/
│   └── styles.css      # all styling
├── images/
│   └── kuma-portrait.jpg
└── fav.ico
```

## Running it locally

No tooling required — open `index.html` in a browser. To serve it over HTTP
instead:

```bash
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## Deploying

GitHub Pages builds automatically on push to `master`. Changes are usually
live within a minute.

---

© Kuma Lawrence. Design and content are mine; please don't republish the
page as your own.
