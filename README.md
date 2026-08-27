# Harborview Signage

A static, serverless prototype for a Wi-Fi-hosted digital signage system.

## Included

- Admin login and dashboard
- Content editor for policy of the week, celebrations, audit results, photos, and ticker messages
- TV player route at `#/player`
- Clock and weather widget placeholder
- Kiosk launch with fullscreen request and Screen Wake Lock where supported
- PWA manifest and offline cache
- Responsive layout for desktop admin and landscape TV displays

## Run

This project has no Node runtime dependency. Open `index.html` directly for a quick preview. For PWA features and Wake Lock, host the folder over HTTPS or from the common Wi-Fi portal.

Demo login: `admin@harborview.local` / `admin123`

## TV deployment

Use the player URL:

`https://YOUR-PORTAL/index.html#/player?kiosk=1`

The Android TV wrapper should launch this URL on boot, keep the app in immersive mode, and acquire a screen Wake Lock. Android TV device-management policy or a kiosk launcher is still required to guarantee auto-launch and disable the screensaver on every Philips model.

## GitHub Pages hosting

Create a GitHub repository, upload this project, and push the `main` branch. In the
repository settings, open **Pages**, choose **GitHub Actions** as the source, then wait
for the **Deploy web app to GitHub Pages** workflow to finish. The player URL will be:

`https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/index.html#/player?kiosk=1`

## Production next steps

Replace localStorage with a shared REST/Supabase/Firebase backend, add real authentication, upload storage, playlist scheduling, device heartbeats, and a weather API. The static UI is intentionally ready for those services without requiring a Node server.
