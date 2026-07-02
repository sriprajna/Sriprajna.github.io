# Sriprajna KJ — Portfolio (Static Build for GitHub Pages)

A modern, editorial-style portfolio built with React + TailwindCSS.
Fully static — works on GitHub Pages, Netlify, Vercel, S3, or any static host.

## What's inside

- `index.html` — entry point
- `404.html` — fallback for GitHub Pages
- `static/` — bundled CSS + JS + assets
- `asset-manifest.json` — build manifest
- `README.md` — this file

Total size: ~1 MB (gzipped).

## Deploy to GitHub Pages

### Option A — User site (`sriprajna.github.io` repo)

1. Clone your `sriprajna.github.io` repo locally.
2. Move existing content to a backup branch if you want to keep it.
3. Copy all files from this ZIP (not the folder itself) into the repo root.
4. Commit and push:
   ```bash
   git add .
   git commit -m "Deploy new portfolio"
   git push origin main
   ```
5. Live at `https://sriprajna.github.io/` in ~1 minute.

### Option B — Project site (any repo)

1. Create a new repo (e.g., `portfolio`).
2. Copy all files from this ZIP to the repo root.
3. Push to `main`.
4. Settings → Pages → source: `main` branch, `/root`.
5. Live at `https://sriprajna.github.io/portfolio/`.

Both options work with no code changes because `homepage` is set to `"."`.

## Routing

Uses `HashRouter` (URLs like `/#/projects/ai-native-engineering-enablement-program`) so no server-side rewrite config is needed on GitHub Pages.

## Contact form & resource downloads

Both flows open the visitor's default email client (mailto:) with the message prefilled to `sriprajna@gmail.com`. No backend is required.

To upgrade later, wire the form submissions to Formspree, Netlify Forms, or your own backend by editing `Contact.jsx` and `Resources.jsx` before rebuilding.

## Resume PDF

The "Download Resume" button in the Hero generates a multi-page professional PDF client-side using jsPDF. Content is sourced from `mock.js` — edit and rebuild to update.

## Rebuilding from source

```bash
cd frontend
yarn install
yarn build
```

The `build/` folder can be re-uploaded to your GitHub Pages repo.

---

Design inspiration: modern editorial portfolios. Fonts: Fraunces (headings) + Inter (body). Icons: lucide-react.
