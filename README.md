# Isavio Group

A single-page app for Isavio Group — a welcome screen, a venture-selection screen (four ventures, one live), and a showcase page for the Website Building venture (Ishan Srivastava & Avi Jaiswal).

It's a single static file (`index.html`, all images inlined as base64) — no build step, no dependencies.

## Run it locally

Just open `index.html` in a browser, or serve it:

```bash
npx serve .
```

## Deploy to GitHub

```bash
cd isavio-app
git init
git add .
git commit -m "Isavio Group site"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

## Deploy to Vercel

**Option A — Vercel CLI**

```bash
npm i -g vercel
cd isavio-app
vercel
```
Follow the prompts (link/create a project, keep defaults — it's a static site, no build command needed). Then run `vercel --prod` to publish.

**Option B — Vercel dashboard**

1. Push this folder to a GitHub repo (see above).
2. Go to [vercel.com/new](https://vercel.com/new) and import the repo.
3. Framework preset: **Other** (static). Leave build command empty, output directory as root.
4. Click **Deploy**.

Either way, Vercel serves `index.html` at your root URL automatically — no extra config needed beyond the included `vercel.json`.

## Structure

```
isavio-app/
├── index.html      # the whole app (HTML + CSS + JS + images inline)
├── vercel.json      # static-site config
├── .gitignore
└── README.md
```
