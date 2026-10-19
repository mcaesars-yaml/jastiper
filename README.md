# Jastip Book

A personal mobile app for running jastip trips: orders, foreign-currency → IDR pricing, fees,
DP / full payments, shopping list, and WhatsApp bills. Plain HTML/JS PWA — no build step,
no server, works offline. All data stays on the phone (`localStorage`); back it up to Google Drive
from **More → Back up now**.

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole app (UI, logic, styles) |
| `sw.js` | Service worker — offline cache |
| `manifest.webmanifest` | Install-to-home-screen metadata |
| `icon.svg`, `icon-*.png` | App icons |

## Hosting (GitHub Pages)

1. Repo **Settings → Pages → Build and deployment → Source: Deploy from a branch**, branch `main`, folder `/ (root)`.
2. Open `https://mcaesars-yaml.github.io/jastiper/` on your phone.
3. iPhone: Safari → Share → **Add to Home Screen**. Android: Chrome → ⋮ → **Install app**.

## Updating the app

After changing any file, bump `CACHE` in `sw.js` (e.g. `jastip-v1` → `jastip-v2`) so installed
phones pick up the new version. Open the app twice after deploying to load the update.

## Run locally

```bash
python3 -m http.server 8000
```
Then open http://localhost:8000.
