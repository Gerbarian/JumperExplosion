# Short n' Sweet Flappy

One-tap Flappy tension, rebuilt as high-fashion chaos. Same pure loop — flap, thread the gap, don’t die — but snappier physics, living gates, graze payouts, and pressure that goes electric as the score climbs.

Single static page. Deploys anywhere. Easy to wrap later for iOS.

## How to play

- **Tap or click anywhere** to flap. That’s the only control.
- Pass chrome gates to score. Combo climbs the longer you stay clean (**x1 → x5 Overdrive**).
- **Graze** a lip for a fat bonus, a visual slam, and extra heat.
- **Surges** kick in as you climb: tighter hot gates, more speed, more points.
- One hit ends the run. Tap to retry immediately.
- Best score is saved on device. Ranks: Spark (10), Volt (25), Icon (50), Void (100).

## Tech stack

- Vanilla **HTML + CSS + JavaScript**
- **Canvas 2D** (no images, fonts, libraries, or CDNs)
- `localStorage` for best score
- Optional `navigator.vibrate` haptics (silent fallback on iOS)

## Deploy (Netlify)

1. Point the Netlify site at this repository.
2. Leave the build command empty.
3. Set the publish directory to the repo root (`/`).
4. `index.html` is the site entry. No bundler or Node build is required.

Locally, open `index.html` in a browser or serve the folder with any static server.

## iOS / Capacitor

Designed to be easily wrapped with Capacitor for iOS App Store.

WKWebView-safe APIs only (Canvas, touch/pointer input, localStorage, Web Audio after a gesture). Drop `index.html` into a Capacitor web root and optionally swap `haptic()` for `@capacitor/haptics`.
