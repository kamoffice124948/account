# Madrasah Accounts (Web App)

Student account management for a madrasah — runs entirely in the browser, works offline, installable as an app (PWA). No server, no build step.

## Publish on GitHub Pages
1. Create a new GitHub repository and upload all files in this folder (keep the `.github` folder and `.nojekyll`).
2. Go to **Settings → Pages → Build and deployment → Source: GitHub Actions**.
3. Push to `main`. After ~1 minute the app is live at `https://<username>.github.io/<repo>/`.

(Alternative without Actions: Settings → Pages → Source: *Deploy from a branch* → `main` / `(root)`.)

## Install on phone / PC
Open the site in Chrome/Edge → menu → **Install app** / **Add to Home screen**.

## Data & backup
- Data is stored in the browser on that device (localStorage). Clearing site data erases it, so **always set up backups**: Import / Export tab → *Choose backup folder* (Chrome/Edge on desktop), or export a backup file regularly.
- Restore: Import / Export → *Restore backup*.
- Direct Google Drive sign-in now works because the site is served over https — create a Google Cloud OAuth Web Client ID, add your `https://<username>.github.io` as an authorized JavaScript origin, and paste the Client ID in the app.
- Excel (.xlsx) and CSV import/export work offline.

## Files
- `index.html` – the whole app
- `manifest.webmanifest`, `sw.js`, `icons/` – installable/offline support
- `.github/workflows/pages.yml` – auto-deploy
