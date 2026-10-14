# Nested · case study

A scroll-story case study for **Nested**, a mobile CRM for real-estate Relationship Managers, by Manish Ray.

Static site: one `index.html` plus two images in `assets/`. No build step, no dependencies.

## Run locally

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy

Pushing to `main` deploys to GitHub Pages through `.github/workflows/pages.yml`.
One-time setup: repo **Settings → Pages → Build and deployment → Source: GitHub Actions**.

The site will be at `https://<username>.github.io/<repo-name>/`.
