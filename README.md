# LiftLog

A workout tracker that works completely offline. No account, no server, no internet needed once it's on your phone. Everything you log stays on your device.

## What it does

LiftLog works like a personal trainer that lives on your phone. It remembers every set, raises the difficulty for you, runs the timers, and tells you what to do next and **why**.

**Coaching**
- **Automatic progressive overload:** rate each exercise Easy, Good or Hard (and flag if form broke down). LiftLog combines that with your reps and history to add a rep, add weight, repeat, or back off, and explains every change.
- **Learns each lift:** lifts that handle increases well move faster; lifts that stall wait longer at the top of the range.
- **Deload weeks:** spots when you've been struggling and suggests a lighter week.
- **Short on time:** tell it you have 45, 30, 25 or 20 minutes and it trims accessories first, keeping your main lifts.
- **Weekly schedule:** pick training days; miss one and the week reshuffles.
- **Muscle recovery map:** estimated readiness per muscle group, with a warning if today's routine targets sore muscles.

**During the workout**
- **Autopilot:** one set at a time, targets preloaded, one big Done button, auto-advance.
- **Exercise modes:** weight + reps, bodyweight reps, timed holds, distance (carries, sled), EMOM / intervals, and a tempo guide with audio cues.
- **Smart rest timers** per exercise, with beeps and vibration.
- **Swap:** machine taken? Get equivalent exercises for the equipment you have, with an estimated starting weight.
- **Plate calculator:** plates per side shown under every barbell set.
- **Hands-free:** optional voice coach reads your next set; voice commands ("done", "what's next", "skip rest", "135 pounds"...).

**Tracking**
- **Equipment profiles:** gym, home, travel. Routines adapt automatically.
- **Records** for weight, estimated 1-rep max, reps, holds and distance.
- **Progress charts** per exercise and weekly volume.
- **Backup and restore** as copy-paste text.

See [ROADMAP.md](ROADMAP.md) for how the phases were built and the one feature (watch app) that needs a native app.

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
