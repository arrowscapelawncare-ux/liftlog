# LiftLog

A workout tracker that works completely offline. No account, no server, no internet needed once it's on your phone. Everything you log stays on your device.

## What it does

- **Log workouts:** pick exercises, enter weight and reps, and tap ✓ for each set. Each set shows what you lifted last time.
- **Rest timer:** starts on its own after each set, with +15s, −15s and Skip. It vibrates and beeps when time is up (where the phone allows).
- **Routines:** save any finished workout as a routine and start it again with one tap.
- **History and PRs:** every workout with its time, total volume and best sets. New personal records get a PR badge (estimated 1-rep max, Epley formula).
- **Exercise library:** 34 common lifts plus your own custom exercises, with stats for each.
- **Backup and restore:** copy your whole log as text and paste it back on any device.
- **Light and dark mode:** follows your phone's setting.

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
