# Short n' Sweet Flappy

A modern, highly addictive Flappy Bird evolution themed around Sabrina Carpenter. Float through espresso-shot pipes, chain clean passes for combo multipliers, and skim the foam for near-miss bonuses.

Built as a single static page so it deploys anywhere and can later ship as a native iOS app with minimal changes.

## How to play

- **Tap or click anywhere** to flap.
- Weave through the espresso shots. Each pass scores points.
- **Near-miss:** skim close to a pipe lip for **+2** and a gold flash.
- **Combo:** consecutive clean passes climb **x1 → x2 → x3**.
- One hit ends the run. Tap again to restart instantly.
- High score is saved on device. Medals: Bronze (10), Silver (25), Gold (50), Platinum (100).

## Tech stack

- Vanilla **HTML + CSS + JavaScript**
- **Canvas 2D** rendering (no images, fonts, libraries, or CDNs)
- `localStorage` for best score
- Optional `navigator.vibrate` haptics (no-ops gracefully on iOS)

## Deploy (Netlify)

1. Point the Netlify site at this repository.
2. Leave the build command empty.
3. Set the publish directory to the repo root (`/`).
4. `index.html` is the site entry. No bundler or Node build is required.

Locally, open `index.html` in a browser or serve the folder with any static server.

## iOS / Capacitor

Designed to be easily wrapped with Capacitor for iOS App Store.

The game already uses a WKWebView-safe subset of the web platform (Canvas, touch/pointer input, localStorage, Web Audio after a user gesture). Drop `index.html` into a Capacitor web root, then optionally swap the isolated `haptic()` helper for `@capacitor/haptics` for native iPhone feedback.
