Sales & Activity Dashboard — PWA Package
========================================

This is a Progressive Web App (PWA) build of your dashboard. It supports:
- Add to Home Screen (iOS/Android/Desktop)
- Offline usage after first load (service worker caching)
- Local storage of your data and goals

Files
-----
- index.html               The dashboard
- manifest.webmanifest     PWA metadata
- sw.js                    Service worker for caching
- icon-192.png, icon-512.png  App icons

Quick Deploy (GitHub Pages)
---------------------------
1) Create a new repository named `sales-dashboard` on GitHub.
2) Upload all files from this folder to the repository root.
3) In repo Settings → Pages → Deploy from `main` branch → `/ (root)`.
4) After it publishes, open your site URL on your phone.
5) Install:
   - Android/Chrome: ⋮ menu → "Install app"
   - iOS/Safari: Share → "Add to Home Screen"
   - Desktop Chrome/Edge: Install icon in address bar

Local Test (Mac/Windows)
------------------------
You need to serve over HTTP(S) for the service worker to work.
- Python 3: `python -m http.server 8000` then open http://localhost:8000/
- Node: `npx http-server -p 8000`

Notes
-----
- Service workers require HTTPS (or localhost). Opening the file directly (file://) will not register the SW.
- Your data remains in your browser’s local storage. Use the built-in backup to export JSON.