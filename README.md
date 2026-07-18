# Retune — marketing site

A single static `index.html` (no build step, no dependencies) for the Retune landing page,
hosted on **Vercel** (Creatix team) at tryretune.com.

## App is live
Retune shipped on the App Store on 2026-07-17:
https://apps.apple.com/us/app/retune-guitar-tuner/id6789782801 (app id `6789782801`).
The hero uses Apple's official "Download on the App Store" black badge
(`app-store-badge.svg`, from Apple's marketing tools; per the guidelines: don't restyle,
min 40px tall, quarter-height clear space, one badge per layout). Pages also carry a
`apple-itunes-app` meta tag for Safari's Smart App Banner.

## Deploy to GitHub Pages (free, ~3 minutes)
1. Create a **new public repo** on GitHub named `retune-site`.
   (Public keeps Pages free on any plan; your *app* repo can stay private separately.)
2. Push this folder to it:
   ```sh
   cd retune-site
   git init
   git add .
   git commit -m "Retune landing page"
   git branch -M main
   git remote add origin https://github.com/<you>/retune-site.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Build and deployment**.
   Source: **Deploy from a branch**. Branch: **main**, folder: **/ (root)**. Save.
4. Wait ~1 minute. Your site is live at
   `https://<you>.github.io/retune-site/`.

## Custom domain (optional, later)
If you buy a domain (e.g. `retune.app`):
1. Settings → Pages → **Custom domain** → enter it (this creates a `CNAME` file — commit it).
2. At your registrar, add a CNAME record pointing `www` → `<you>.github.io`, and the four
   `A` records GitHub lists for the apex domain.
3. Tick **Enforce HTTPS** once the cert provisions.

## Local preview
Just open `index.html` in a browser, or run `python3 -m http.server` in this folder and
visit `http://localhost:8000`.
