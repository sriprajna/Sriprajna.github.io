# Sriprajna KJ — Portfolio (Static Build for GitHub Pages)

A modern, editorial-style portfolio built with React + TailwindCSS. This build is a **fully static site** with no backend dependency — it works on GitHub Pages, Netlify, Vercel, S3, or any static host.

## What's in this ZIP

- `index.html` — entry point
- `static/` — bundled CSS + JS + assets
- `asset-manifest.json` — build manifest
- `README.md` — this file

Total size: ~1 MB (gzipped).

## Deploy to GitHub Pages (Recommended)

You have two options depending on your repo type:

### Option A — User site (`sriprajna.github.io` repo)

1. Clone your `sriprajna.github.io` repo locally.
2. Delete existing content (or move it to a branch as backup).
3. Copy **all files inside this ZIP** (not the folder itself) to the repo root.
4. Commit and push to `main`:
   ```bash
   git add .
   git commit -m "Deploy new portfolio site"
   git push origin main
   ```
5. Site goes live at `https://sriprajna.github.io/` within 1–2 minutes.

### Option B — Project site (any repo, served at `sriprajna.github.io/repo-name/`)

1. Create a new repo (e.g., `portfolio`).
2. Copy all files from this ZIP to the repo root.
3. Push to `main`:
   ```bash
   git add . && git commit -m "Deploy portfolio" && git push origin main
   ```
4. Go to repo → **Settings → Pages** → source: `main` branch, `/root`.
5. Site goes live at `https://sriprajna.github.io/portfolio/`.

The build uses `"homepage": "."` so **both options work with no changes needed**.

## Routing

The site uses `HashRouter` (URLs like `/#/projects/dell-data-engineering-course-suite`) which works out-of-the-box on GitHub Pages without needing a 404.html rewrite.

## Contact Form & Resource Requests

- **Contact form**: on submit, opens the visitor's email client (mailto:) with the message prefilled to `sriprajna@gmail.com`.
- **Resource downloads**: each resource card asks for name + email, then opens a mailto: request to `sriprajna@gmail.com`.

To upgrade later to real form submission storage:
1. Add SendGrid/Formspree/Netlify Forms.
2. Update `Contact.jsx` and `Resources.jsx` to POST to your service endpoint.

## Resume PDF

The "Download Resume" button in the Hero generates a professional PDF client-side using jsPDF from the data in `mock.js` — no server needed. To update the resume content, edit the experience/certifications/profile in `mock.js` and re-run the build.

## Rebuilding from source

The full source (React + FastAPI backend for optional lead capture) lives in the parent project. To rebuild:
```bash
cd frontend
yarn install
yarn build
```
The `build/` folder can be re-uploaded to GitHub Pages.

---

Portfolio design inspired by editorial layouts. Fonts: Fraunces (headings) + Inter (body). Icons: lucide-react.
