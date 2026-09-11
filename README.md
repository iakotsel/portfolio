# Iakovos Tselentis — Portfolio

A single self-contained `index.html` (no build step, no dependencies) with a light/dark toggle, a changelog-style career timeline, project case studies, and a writing section.

## Deploy to GitHub Pages

1. Create a new repo (e.g. `iakovos-portfolio`) on GitHub.
2. Add these files to it:
   - `index.html`
   - `assets/` (drop your real images here — see below)
3. Push to the `main` branch.
4. In the repo, go to **Settings → Pages**, set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`. Save.
5. GitHub gives you a URL like `https://<your-username>.github.io/iakovos-portfolio/` within a minute or two.

Want a custom domain later? Add a `CNAME` file with your domain name at the repo root and point your DNS at GitHub's Pages servers — GitHub's docs walk through the exact records.

## Adding your real images

The page currently shows dashed placeholder boxes for screenshots and photos. Drop files into `assets/` using these exact names and each placeholder becomes a real `<img>`:

- `assets/proj-fusion.jpg` — Fusion MVP screenshot
- `assets/proj-ax.jpg` — AX / D365 interface
- `assets/proj-pbi.jpg` — Power BI dashboard
- `assets/culture-mvp.jpg` — MVP 2025 award photo
- `assets/culture-24h.jpg` — 24-hour challenge photo

Then in `index.html`, replace each `<div class="media-slot" ...>...</div>` with:
```html
<img src="assets/proj-fusion.jpg" alt="Fusion MVP screenshot">
```
(swap in the matching filename/alt text for each one).

## Still to confirm before it's public

The page itself has a small note block near the footer listing open items (a partner-bank detail to confirm, and the screenshots above). Delete that `<div>` once everything's resolved.

## Editing

It's plain HTML/CSS/JS — open `index.html` in any editor. Colors and fonts are CSS custom properties at the top of the `<style>` block (`--color-*`, `--font-*`), so a palette or font change is a few line edits, not a rewrite.
