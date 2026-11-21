# LiftLog

A workout tracker that works completely offline. No account, no server, no internet needed once it's on your phone. Everything you log stays on your device.

## What it does

LiftLog works like a personal trainer that lives on your phone. It remembers every set, raises the difficulty for you, runs the timers, and tells you what to do next and **why**.

- **Automatic progressive overload:** rate each exercise Easy, Good or Hard (and flag if form broke down). LiftLog combines that with your actual reps and history to set your next target: add a rep, add weight, repeat, or back off. Every suggestion explains itself, e.g. *"Increase 5 lb. You reached the top of your rep range (10) on every set with good technique."*
- **Today's plan:** before you start, see the estimated duration and a coach note for every exercise.
- **Autopilot workouts:** one set at a time, weights and reps preloaded, one big Done button. It moves to the next set and exercise on its own.
- **Exercise types:** weight + reps, bodyweight reps, and timed holds (planks go 30 → 35 → 40 s automatically, with a countdown).
- **Smart rest timers:** each exercise has its own rest (heavy squats 3:00, curls 1:00). Beeps in the last 3 seconds and vibration where the phone allows.
- **Voice coach (optional):** reads your next set aloud when rest ends.
- **Check-in:** energy, soreness and difficulty in three taps at the end.
- **Records:** heaviest weight, estimated 1-rep max, best set, most reps, longest hold.
- **Routines:** build your own; "Up next" rotates through them.
- **Backup and restore:** copy your whole log as text and paste it back on any device.

See [ROADMAP.md](ROADMAP.md) for what's coming in phases 2 to 4.

## Use it offline

LiftLog is a Progressive Web App:

1. Open the hosted page once while online. The app caches itself on that visit.
2. Install it:
   - **Android (Chrome):** menu ⋮ → **Add to Home screen** / **Install app**
   - **iPhone (Safari):** Share → **Add to Home Screen**
3. From then on it opens from your home screen with no connection.

You can also download `index.html` and open it straight from your phone's files. It runs with no internet that way too.

## Host it with GitHub Pages

Settings → Pages → Source: **Deploy from a branch** → Branch: `main`, folder `/ (root)` → Save. The site appears at `https://<your-username>.github.io/liftlog/` within a minute or two.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole app: layout, styles and logic in one file |
| `manifest.webmanifest` | App name, colors and icons for installing to the home screen |
| `sw.js` | Service worker that caches the app so it opens offline |
| `icons/` | App icons (SVG, 192px and 512px PNG) |

## Your data

Workouts are saved in your browser's local storage on that device only. Nothing is sent anywhere. Clearing your browser's site data erases the log, so use **Settings → Copy backup** now and then.
