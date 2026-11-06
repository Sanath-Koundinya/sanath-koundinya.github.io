# sanath-koundinya.github.io

My Personal site!

## What's in here

```
index.html      the whole site — markup, styles, and script in one file
favicon.svg     small hand-drawn dragon mark used as the browser tab icon
404.html        matches the site style, shown for broken/missing links
robots.txt      tells search engines the site is crawlable
sitemap.xml     one-page sitemap
resume.pdf      
```

## Editing content

You shouldn't need to touch the CSS or the page structure for routine updates — the same instructions are also in a comment at the top of `index.html`:

- **Projects** — edit the `PROJECTS` array in the `<script>` at the bottom of `index.html`.
- **Skills** — edit the `SKILLS` array, right next to it.
- **Email / GitHub / LinkedIn** — edit the `LINKS` object. Also update the matching `og:`/`twitter:` meta tags and the JSON-LD block near the top of `<head>`, and the `href`s in the hero and contact sections, so everything stays in sync.
- **Today I Learned entries** — edit the `TIL_ENTRIES` array, same pattern.
- **About / Now / Involvement / Education** — plain text further down the HTML body; find the section by its comment header.
- **Resume** — drop a file named `resume.pdf` in the repo root. The "Resume" links in the hero and contact section already point at it.

