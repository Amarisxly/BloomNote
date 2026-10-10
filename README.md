# Bloomnote PWA

Upload this whole folder to any HTTPS static host, then open the address on your phone and add it to your home screen.

## Hosting (pick one)

- **Netlify Drop**: go to app.netlify.com/drop and drag the `bloomnote-pwa` folder onto the page.
- **GitHub Pages**: push these files to a repository, then Settings › Pages › Deploy from branch.
- **Vercel / Cloudflare Pages**: create a project from the folder; no build step is needed.

## Install

- **iPhone (Safari)**: Share › Add to Home Screen.
- **Android (Chrome)**: menu › Install app, or Settings › Install Bloomnote inside the app.

## Files

| File | What it does |
|---|---|
| `index.html` | The whole app |
| `manifest.webmanifest` | Name, colours and icons for the home screen |
| `sw.js` | Offline support: caches the app and fonts |
| `icons/` | App icons (192, 512, maskable 512, Apple touch, favicon) |

## Notes

- Bouquets, cards, album pages and your own flowers are stored on the device (localStorage). They are not synced, and data from the Claude artifact version does not carry over.
- Save image uses the phone's share sheet when available (choose Save Image), otherwise a normal download.
- After changing `index.html`, bump `VERSION` in `sw.js` so installed copies update.
- Opening `index.html` directly from disk works, but offline install needs an `http(s)` address.
