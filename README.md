# Pocket Ledger

A white-label income and expense tracker. Plain HTML/CSS/JS, no build step, works offline.

## Rebranding
Edit `config.js`: business name, tagline, brand colour, currency, locale, income and expense categories. Then bump `CACHE_VERSION` in `sw.js`.

## Replacing icons
Replace `icon-192.png` and `icon-512.png` with your own (same filenames, same sizes). A simple SVG source is in this README's history or design your own.

## Hosting on free tiers
- **GitHub Pages**: upload files, Settings → Pages → Deploy from `main` / root.
- **Netlify**: drag the folder onto app.netlify.com/drop.
- **Cloudflare Pages**: connect repo, no build command, output dir = root.

## Install on Android
Open the URL in Chrome → menu (⋮) → **Install app**.

## Install on iPhone
Open in Safari → Share → **Add to Home Screen**.

## Backing up data
More tab → **Download JSON backup**. Restore via **Restore from backup** (warns how many entries will be replaced). CSV export is also available.

## Shipping updates
Change `CACHE_VERSION` in `sw.js` (e.g. `v1` → `v2`). Commit. Existing users will see an **Update** button; they reload only after tapping it.

## Troubleshooting
- **Blank page**: `index.html` must be at repo root, not in a subfolder.
- **No install button**: needs HTTPS (Pages/Netlify provide it) and a valid `manifest.json` + icons.
- **Offline not working**: open the URL online once so the service worker caches the shell.
- **Stale version after edit**: bump `CACHE_VERSION`.

## Licence
Unlimited client deployments allowed. **Reselling the template itself is not permitted.**