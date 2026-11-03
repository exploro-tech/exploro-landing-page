# exploro.in — Christmas launch countdown

Coming-soon page for **exploro** ("Closer to what you need"), counting down to launch at **00:00 IST, 25 December 2026**.

It's a static site with no build step. Upload the folder as it is to any static host (GitHub Pages, Netlify, Vercel or Cloudflare Pages).

## Files

| Path | What it is |
|---|---|
| `index.html` | The page: markup, styles, countdown, Santa, snow and gift logic |
| `support.js` | Small runtime that renders the page (uses React) |
| `vendor/` | React 18.3.1, ReactDOM 18.3.1 and Babel standalone 7.29.0, served locally |
| `assets/` | Logo, 3D room render, Santa sleigh, favicons, social preview (`og-xmas.jpg`) |
| `robots.txt`, `sitemap.xml` | SEO |

## Features
- A live countdown (days, hours, minutes, seconds). When the timer reaches zero, the page switches to "We're live. Merry Christmas!" and shows a **Start exploring** button.
- Santa's sleigh follows the cursor. After 3.5 s idle, or on touch screens, he flies on his own.
- Clicking or tapping drops a gift. Gifts bounce and **stay on the snow**; up to 80 are kept.
- Snow drifts with the mouse, string lights twinkle across the top, and the moon, stars and aurora glow.
- Fully responsive: on screens 900 px wide and below, the page stacks into a single column.
- Respects `prefers-reduced-motion`: with it on, there's no Santa, snow or gifts, but the countdown still runs.

## Editing
- **Launch time:** `var LAUNCH = new Date('2026-12-25T00:00:00+05:30')` in the script near the bottom of `index.html`.
- **Social links:** search for `instagram.com/exploro_india` and `linkedin.com/company/exploro-india`.
- **Analytics:** paste your DataFast snippet where the comment says so in `<head>`.

## Run locally
```
npx serve .        # or: python3 -m http.server
```
Open the page through a local server, not by double-clicking `index.html` (opening it with `file://` won't work).
