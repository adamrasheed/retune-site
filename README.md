# Retune — marketing site

A single static `index.html` (no build step, no dependencies) for the Retune landing page,
hosted free on **GitHub Pages**.

## Before you publish
Edit `index.html` and replace the placeholders:
- `you@example.com` → your real contact email (appears in the "Notify me" button + footer).
- Swap the working name **Retune** once you finalize it (search-and-replace the word).
- When the app is live, change the hero "Notify me" button to an **App Store** link.

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
