# Short n' Sweet Ascent

A vertical one-tap climber. Gravity drags you down. You flap to rise. The camera chases altitude through a 2.5D shaft of shifting apertures — not a side-scrolling Flappy clone.

Single static page. Deploys anywhere. Easy to wrap later for iOS.

## How to play

- **Tap or click** to flap. That’s the only control.
- Tap **left or right of your first tap** to veer. Same spot = straight up.
- Thread 3D gates, hoops, sweepers, and dual lanes as you climb.
- **Graze** a rim or hit **Perfect** center for extra score.
- Combo climbs **x1 → x5 Overdrive**. Surges drop hotter, tighter gates.
- Fall off the bottom or clip a gate and you’re done. Tap to rise again.
- Score and **altitude** are saved. Ranks: Spark 15 / Volt 40 / Icon 80 / Apex 140.

## Tech stack

- Vanilla **HTML + CSS + JavaScript**
- **Canvas 2D** with perspective projection, parallax, and camera roll (no images, fonts, libraries, or CDNs)
- `localStorage` for best score and best altitude
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
