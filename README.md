# Priyam Srivastava & Associates – website

A static, single-page website (no build step, no dependencies).

## Files

| File | Purpose |
|------|---------|
| `index.html` | Page structure, header, footer and enquiry popup |
| `style.css` | All styling (light and dark mode) |
| `script.js` | Practice-area content, page routing, menu and enquiry form logic |

## Run locally

Option 1 – just double-click `index.html`.

Option 2 – run a small local server (recommended):

```bash
# Python 3
python -m http.server 8000
# or Node.js
npx serve .
```

Then open http://localhost:8000

## Edit common things

- **Phone number:** footer in `index.html` (search for `tel:`).
- **Google Form link:** `FORM_URL` near the bottom of `script.js`.
- **Practice areas:** the `S` list at the top of `script.js`.
- **Founder bio:** the `people` section inside `view()` in `script.js`.

## Host on GitHub Pages

1. Push these files to a GitHub repository.
2. Go to **Settings → Pages**, choose the `main` branch and the root folder, and save.
3. Your site will be live at `https://<username>.github.io/<repo>/`.

## Deploy on Vercel

This is a static site, so no framework or build settings are needed. `vercel.json` is already included.

**Option A – from GitHub (recommended)**

1. Push these files to a GitHub repository (files at the repo root).
2. On vercel.com choose **Add New → Project** and import the repository.
3. Leave **Framework Preset** as `Other`, and leave the Build Command and Output Directory empty.
4. Click **Deploy**. Every future `git push` redeploys automatically.

**Option B – Vercel CLI (no GitHub needed)**

```bash
npm i -g vercel
cd priyam-srivastava-associates
vercel        # first deploy (preview)
vercel --prod # production deploy
```

To use your own domain, open the project on Vercel and go to **Settings → Domains**.
