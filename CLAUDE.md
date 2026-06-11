# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Zaya's Landscaping — single-page static website hosted on GitHub Pages with custom domain https://zayaslandscapinghawaii.com/

No build step, no framework, no dependencies. Edit `index.html` directly and push to deploy.

## Deploy

```
git add <files>
git commit -m "message"
git push origin main
```

GitHub Pages serves from the `main` branch root. Changes are live within 1–3 minutes.

## Architecture

Everything is in a single file: `index.html`

Internal order matches the page layout:
1. `<style>` — all CSS, organized by section with `/* ── SECTION ── */` comments
2. `<nav>` — fixed top nav with mobile hamburger toggle
3. `#hero` — full-viewport hero with logo background + gradient overlay
4. `#services` — 6 service cards in an auto-fit grid
5. `#why` — 4 stat items on dark green background
6. `#about` — flex row: text left, logo image right
7. `#gallery` — 9-item grid with lightbox (first item spans 2 columns)
8. `#testimonials` — 6 review cards on dark green background
9. `#contact` — Formspree form (endpoint: xkoaqjgy), phone: (808) 302-4437
10. `#lightbox` — fixed overlay, controlled by JS
11. `<footer>`
12. `<script>` — inline JS for nav toggle, gallery lightbox, and Formspree AJAX submit

## Images

All images are local files committed to the repo root:

| File | Used in |
|---|---|
| `zayas-landscaping.jpg` | Hero background + About section |
| `zayaslandscaping.png` | Nav logo (48px circle) |
| `IMG_3721.JPG` | Gallery slot 0 (wide, spans 2 cols) |
| `IMG_4147.JPG` | Gallery slot 1 |
| `IMG_0127.JPG` | Gallery slot 2 |
| `IMG_8922.JPG` | Gallery slot 3 |
| `landscaping.jpg` | Gallery slot 4 |
| `IMG_0338.JPG` | Gallery slot 5 |
| `IMG_3712.JPG` | Gallery slot 6 |
| `IMG_4130.JPG` | Gallery slot 7 |
| `IMG_8044.JPG` | Gallery slot 8 |

## SEO

- Custom domain: zayaslandscapinghawaii.com (CNAME file in repo root)
- Canonical URL, Open Graph, Twitter Card meta tags in `<head>`
- JSON-LD `LandscapingBusiness` structured data
- `robots.txt` and `sitemap.xml` in repo root
- Sitemap URL for GSC: https://zayaslandscapinghawaii.com/sitemap.xml
