# SKapi.pro Landing Page

Static landing page for [skapi.pro](https://skapi.pro/). Single-file HTML with inline CSS, no build step.

## Deploy

Upload to Hostinger hPanel → File Manager → `domains/skapi.pro/public_html/`:

- `index.html` → root
- `robots.txt` → root
- `sitemap.xml` → root
- `main.js` → root (if present)
- `make-color.webp` / `n8n-color.webp` → root (if present)

### Post-deploy

- Set up 301 redirect: `www.skapi.pro` → `https://skapi.pro/` (or vice versa)
- Submit `sitemap.xml` in Google Search Console
- Inspect main page in GSC to clear "Duplicate without user-selected canonical"

## Local Dev

```bash
# any static server works
python3 -m http.server 8080
# open http://localhost:8080
```

## Notes

- `main.js` and `.webp` images are referenced in `index.html` but were not in the original `seo/` directory — they may be hosted on the server already or need to be sourced separately.
- GTM: `G-QB0NSGLNLR`, Meta Pixel: `3062462557296405`
