# Gemini Commercial Broker — Website

Static website. Pure HTML/CSS/JS, no build step.

## Structure
- `index.html` — main page
- `insights/` — articles
- `assets/style.css` — all styles
- `assets/script.js` — minimal JS
- `assets/img/` — logos, favicons, covers

## Local preview
```bash
python3 -m http.server 8000
```

## Deployment
Auto-deployed to gemini-cb.ae via Cloudflare Pages from `main` branch.

## Adding insight
Copy any file from `insights/`, rename, update content. Add card to `insights/index.html` and homepage. Update `sitemap.xml`. Commit & push.
