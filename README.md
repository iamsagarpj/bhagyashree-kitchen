# Bhagyashree Kitchen

Single-page static website for Bhagyashree Kitchen (Satara) — menu browsing, cart, and WhatsApp-based ordering. No backend, no build step. Everything (HTML, CSS, JS) lives in `index.html`.

## Local preview

Just open `index.html` in a browser, or serve it locally:

```
npx serve .
```

## Deploy on Netlify

**Option A — Git integration (recommended)**
1. Push this repo to GitHub (already connected to `origin`).
2. In Netlify: **Add new site → Import an existing project → GitHub** → select this repo.
3. Build command: leave blank. Publish directory: `.` (repo root).
4. Deploy. Netlify picks up `netlify.toml` automatically.

**Option B — Drag and drop**
1. Go to [app.netlify.com/drop](https://app.netlify.com/drop).
2. Drag the whole project folder onto the page.

## Deploy on Vercel

**Option A — Git integration (recommended)**
1. In Vercel: **Add New → Project → Import Git Repository** → select this repo.
2. Framework preset: **Other**. Build command: none. Output directory: `.` (root).
3. Deploy. Vercel picks up `vercel.json` automatically.

**Option B — CLI**
```
npm i -g vercel
vercel --prod
```

## Before going live

Update these placeholders in `index.html`:
- `CONFIG.whatsappNumber` and `CONFIG.upiId` inside the `<script>` block (currently a placeholder UPI ID).
- The Google Maps embed / address block already points to Samarth Mandir Road, Satara.

## Files

- `index.html` — the entire website (production entry point, served at `/`).
- `bhagyashree-kitchen.html` — identical copy, kept for reference.
- `netlify.toml` / `vercel.json` — static hosting config for each platform.
