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

## Changelog

### v2.1 — November 2026
- Rehearsal: edit slide count, total time, and per-slide targets inline without leaving the rehearsal screen
- Rehearsal: redo any individual slide or restart from slide 1 while keeping recorded timings
- Present: pulsing red alert when running significantly over time

### v2.0 — September 2026
- Complete redesign: light/dark adaptive UI (blue accent, Elide/Rescribe visual language)
- Project management: multiple named presentations with cards, open/delete
- Rehearsal mode: per-slide timer with pause, reset, and editable recorded time; timings carry over into configuration
- Back button: browser back navigates within the app (no accidental exit)
- Export / Import JSON: transfer presentations between devices
- Present screen stays dark and full-screen regardless of system theme
- Desktop-first layout for setup and rehearsal; mobile-first for the present screen
- PWA: updated icon (blue), cache version bump

### v1.0 — May 2026
- Single-file timer: configure slides, set target durations, present with live ahead/behind indicator
- Library: save and reload presentations in localStorage
- Time input accepts `3`, `3.22`, and `3:22` formats
- Wake Lock to keep screen on during presentation
- Offline-ready PWA (service worker, installable on Android and iPhone)

## License

MIT
