# sanath-koundinya.github.io

Personal site for Sanath Koundinya — a single static page, no build step, no framework. Everything lives in `index.html`; a few small extra files round it out for a proper GitHub Pages deploy.

## What's in here

```
index.html      the whole site — markup, styles, and script in one file
favicon.svg     small hand-drawn dragon mark used as the browser tab icon
404.html        matches the site style, shown for broken/missing links
robots.txt      tells search engines the site is crawlable
sitemap.xml     one-page sitemap
resume.pdf      not included — add your own (see below)
```

## Preview it locally

No build tools needed — it's plain HTML/CSS/JS. Either:

- Double-click `index.html` to open it directly in a browser, or
- Run a tiny local server from this folder so relative links behave exactly like they will in production:
  ```bash
  python3 -m http.server 8000
  # then visit http://localhost:8000
  ```

## Deploy to GitHub Pages

1. Create a **new GitHub repo** named exactly `Sanath-Koundinya.github.io` (must match your GitHub username, case-insensitive).
2. Upload every file in this folder to the **root** of that repo — `index.html`, `favicon.svg`, `404.html`, `robots.txt`, `sitemap.xml`, and `resume.pdf` once you have one.
3. In the repo, go to **Settings → Pages**, and under "Build and deployment" set the source to **Deploy from a branch**, branch `main`, folder `/ (root)`. (On a lot of repos this is already the default and Pages turns itself on automatically.)
4. Wait a minute or two, then visit `https://sanath-koundinya.github.io`.

Optional: if you ever point a custom domain at this, add a `CNAME` file at the repo root containing just the domain name, and update the `og:url`, `canonical`, and JSON-LD `url` fields in `index.html` to match.

## Editing content

You shouldn't need to touch the CSS or the page structure for routine updates — the same instructions are also in a comment at the top of `index.html`:

- **Projects** — edit the `PROJECTS` array in the `<script>` at the bottom of `index.html`.
- **Skills** — edit the `SKILLS` array, right next to it.
- **Email / GitHub / LinkedIn** — edit the `LINKS` object. Also update the matching `og:`/`twitter:` meta tags and the JSON-LD block near the top of `<head>`, and the `href`s in the hero and contact sections, so everything stays in sync.
- **Today I Learned entries** — edit the `TIL_ENTRIES` array, same pattern.
- **About / Now / Involvement / Education** — plain text further down the HTML body; find the section by its comment header.
- **Resume** — drop a file named `resume.pdf` in the repo root. The "Resume" links in the hero and contact section already point at it.

## Notes

- The site is a single `index.html` on purpose — easy to review as one diff, easy to host anywhere, nothing to build.
- Respects `prefers-reduced-motion` throughout (the entrance animation and the dragon's draw-in both fall back to a static, fully-visible state).
- Includes a print stylesheet, so the page is readable if someone prints it or saves it as a PDF.
