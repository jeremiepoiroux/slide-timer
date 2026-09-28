# Slide Timer

A presentation timer that tracks your pace slide by slide. No dependencies, no build step, no server — one HTML file. Adapts to light and dark mode; the presentation screen is always dark for focus.

## Features

- **Per-slide timing** — set a target duration for each slide; the app shows in real time whether you're ahead or behind
- **Rehearsal mode** — time yourself during practice with pause and reset per slide; record each slide's actual duration and carry those timings directly into your configured run
- **Project management** — save and reload multiple presentations as named projects, stored locally on the device
- **Export / Import** — back up any presentation as a JSON file; share it between devices by transferring the file
- **Offline-ready PWA** — installs on Android and iPhone, works without internet after first load
- **Wake Lock** — screen stays on during a presentation (Chrome / Android)

## Time input format

Slide durations accept three formats:

| Input | Means |
|-------|-------|
| `3` | 3 minutes |
| `3.22` | 3 min 22 sec |
| `3:22` | 3 min 22 sec |

The decimal format (`.`) is handy on mobile keyboards that show `.` instead of `:`.

## Deployment

### Option 1 — Open locally (zero setup)

Download `index.html` and open it in any browser. No server, no install. Data is saved in the browser's local storage.

### Option 2 — GitHub Pages (recommended)

1. Fork this repository
2. Go to **Settings → Pages**
3. Set source to **Deploy from a branch**, select `main`, folder `/` (root)
4. Save — your app is live at `https://your-username.github.io/slide-timer/`

HTTPS is provided automatically, which is required for the PWA and offline support.

### Option 3 — Any static host

Upload `index.html`, `manifest.json`, `sw.js`, and `icon.svg` to any host that serves static files over HTTPS (Netlify, Vercel, Cloudflare Pages, etc.).

## Install as a PWA

### Android (Chrome)

1. Open the app URL in Chrome
2. Tap **⋮ → Add to Home screen** (or accept the install banner)
3. The app installs and runs fullscreen — no browser bar

### iPhone (Safari)

1. Open the app URL in Safari
2. Tap the **Share** button (box with arrow at the bottom)
3. Tap **Add to Home Screen** and confirm

## Data & privacy

All data stays on your device — nothing is sent to any server. Presentations are stored in the browser's `localStorage`, scoped to the PWA origin. Data persists across sessions and app updates.

To transfer a presentation to another device: use **Export JSON** on the source device, then **Import JSON** on the destination.

## License

MIT
