# LiftLog Roadmap

Goal: a lifting app that acts like a personal trainer. It remembers everything, raises the difficulty for you, runs the timers, and always tells you what to do next and **why**. Everything runs offline on the phone; no account, no server.

"Smart" features here are rule-based coaching that runs on the device, not a cloud AI model. That keeps the app fully offline and makes every recommendation explainable.

---

## Phase 1: Coach core (in progress)

The four things that matter every single session.

- [x] **Automatic progressive overload.** Rate each exercise Easy / Good / Hard (plus "form broke down"). LiftLog combines that with your actual reps, weight and history to set the next target, and **every recommendation says why**.
  - Weight + reps: double progression. Add reps inside the target range, then add weight once every set reaches the top.
  - Increases per exercise (e.g. 10 lb squat, 5 lb curl). A bigger jump when you hit the top of the range with reps to spare and rated it Easy.
  - Missed target once or twice: keep the weight and focus on clean reps. Missed 3 sessions in a row (or form broke twice): drop about 10%.
- [x] **Exercise types.** Weight + reps, bodyweight reps, and timed holds (planks go 30 → 35 → 40 s automatically).
- [x] **Rest timers per exercise.** Heavy compound lifts rest longer than curls. The countdown starts on its own with beeps in the last 3 seconds and vibration where the phone allows.
- [x] **Workout autopilot.** One big button per set. Weights and reps are preloaded from the plan, and the app moves on to the next set and exercise by itself. Timed holds count down on their own.
- [x] **Today's workout preview.** Estimated duration, exercise count, and a coach note for each lift ("Bench press: increase 5 lb. You reached the top of your rep range last time.").
- [x] **End-of-workout check-in.** Energy, soreness and difficulty in three taps.
- [x] **Records.** Heaviest weight, estimated 1-rep max, best set, most reps, longest hold.
- [x] **Voice coach (optional).** Reads the next set aloud using the phone's built-in voice.
- [x] **Routine builder.** Create and edit routines; "Up next" rotates through them.

## Phase 2: Gym tools

- [ ] **Plate calculator.** Enter a barbell weight and see the plates for each side (lb and kg plate sets, custom bar weight).
- [ ] **Swap exercise.** Machine taken? Tap Swap for an equivalent movement (same muscle, available equipment), and carry over a sensible starting weight.
- [ ] **Equipment profiles.** Home, commercial gym, travel. Workouts only use what is available.
- [ ] **More exercise modes.** Interval / EMOM (auto-cycling minute timer), tempo training with audio cues (e.g. 3 s down, 1 s up), and distance / carries.
- [ ] **Progress charts.** Estimated strength, volume and records over months for each lift.

## Phase 3: Planning brain

- [ ] **Learned progression rate.** Track how fast each lift actually improves and size increases to match, instead of one rule for everything.
- [ ] **Automatic deloads.** Spot a pattern of struggling across many lifts (misses, Hard ratings, low energy check-ins) and suggest a lighter week.
- [ ] **"I only have 25 minutes."** Shorten a session by trimming sets and accessories first while protecting the main lifts.
- [ ] **Adaptive weekly schedule.** Missed a day? Reshuffle the week while keeping recovery gaps and priorities.
- [ ] **Muscle recovery map.** Body diagram with estimated readiness per muscle from recent volume, soreness check-ins and performance. Always labeled as an estimate.

## Phase 4: Hands-free

- [ ] **Voice commands** ("done", "what's next?", "start rest"). Note: speech recognition in most phone browsers needs an internet connection, so this would be an online-only extra unless built as a native app.
- [ ] **Watch controls.** Needs a native companion app (Wear OS / watchOS); a web app can't run on a watch. Would be a separate project after the phone app is proven.

---

### Design rules

1. Offline first. Everything works with no signal.
2. Explain every change. No silent weight jumps.
3. One-tap logging during the workout. Typing is optional.
4. Safety over speed: repeat or reduce when form breaks down; never push through misses forever.
5. Your data stays on your device, with a text backup you control.
