# Kofe Flow (PWA)

Static files, no build step, no dependencies.

## Run locally
1. Unzip this folder.
2. Open a terminal inside it and run:   python3 -m http.server 8080
   (or:  npx serve .   if you have Node)
3. Open http://localhost:8080 in Chrome, Edge or Safari.

Do not just double-click index.html: service workers (offline mode) only work on
http://localhost or HTTPS. The timer itself still works from file://, but offline/install won't.

## Install / offline
After the first load the app is cached. Chrome/Edge: install icon in the address bar.
iOS Safari: Share > Add to Home Screen.

## Deploy
Upload the whole folder to GitHub Pages, Netlify, Vercel or any HTTPS static host.

## Editing
- Swap the animation: replace assets/timer-loop.webm and assets/timer-loop.mp4 (square, silent, under ~300 KB works best) and assets/poster.jpg.
- After changing any file, bump VERSION in sw.js so returning users get the update.
- Data lives in the browser (IndexedDB + localStorage); clearing site data erases it.
