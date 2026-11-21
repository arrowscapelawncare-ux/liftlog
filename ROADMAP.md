# LiftLog Roadmap

Goal: a lifting app that acts like a personal trainer. It remembers everything, raises the difficulty for you, runs the timers, and always tells you what to do next and **why**. Everything runs offline on the phone; no account, no server.

"Smart" features are rule-based coaching that runs on the device, not a cloud AI model. That keeps the app fully offline and makes every recommendation explainable.

---

## Phase 1: Coach core ✅

- [x] **Automatic progressive overload.** Rate each exercise Easy / Good / Hard (plus "form broke down"). LiftLog combines that with actual reps, weight and history to set the next target, and every recommendation says why.
  - Weight + reps: double progression. Add reps inside the range, then add weight once every set reaches the top.
  - Per-exercise increases (10 lb squat, 5 lb curl); bigger jump when the top of the range was Easy with reps to spare.
  - Missed once or twice: keep the weight. Missed 3 sessions in a row, or form broke twice: drop about 10%.
- [x] **Exercise types:** weight + reps, bodyweight reps, timed holds.
- [x] **Rest timers per exercise** with beeps in the last 3 seconds and vibration.
- [x] **Workout autopilot:** one big button per set, preloaded targets, auto-advance, hold countdowns.
- [x] **Today's plan preview** with estimated duration and a coach note per exercise.
- [x] **End-of-workout check-in:** energy, soreness, difficulty.
- [x] **Records:** heaviest weight, estimated 1-rep max, best set, most reps, longest hold, longest distance.
- [x] **Voice coach:** reads the next set aloud (built-in phone voice, works offline).
- [x] **Routine builder** with an "Up next" rotation.

## Phase 2: Gym tools ✅

- [x] **Plate calculator.** Shows plates per side under every barbell set, plus a full calculator with your bar weight and the plates you own (lb and kg).
- [x] **Swap exercise.** Equivalent movements ranked by movement pattern, exercise type and your history, limited to equipment you have. Starting weight is estimated from the lift you swapped out and labeled as an estimate.
- [x] **Equipment profiles.** Commercial gym, Home and Travel out of the box, fully editable. Routines auto-swap anything that needs missing equipment and say so.
- [x] **More exercise modes.** EMOM / intervals (auto-cycling rounds, missed-round tracking), tempo guide with audio cues (e.g. 3-0-1), and distance work (carries, sled).
- [x] **Progress charts.** Per-exercise trend (estimated 1RM, longest hold, heaviest carry, reps per round) and weekly volume, each with hover/keyboard readouts and a table view.

## Phase 3: Planning brain ✅

- [x] **Learned progression rate.** Each lift tracks how its past weight increases went. Lifts that held every increase move faster; lifts that stalled wait for two sessions at the top of the range.
- [x] **Training blocks.** Choose 4, 5 or 6 weeks of progression; a deload week is planned at the end of each block, then a new block starts.
- [x] **Automatic deloads.** If half or more of your recent lifts were missed or rated Hard (or two check-ins in a row were low energy and hard), LiftLog suggests a lighter week: about 15% less load, one fewer set. Deload sessions don't drag down future targets.
- [x] **"I only have 25 minutes."** Pick 45 / 30 / 25 / 20 minutes on the plan. Accessories lose sets first, then get dropped; main compound lifts are protected. The plan lists exactly what changed.
- [x] **Adaptive weekly schedule.** Choose training days. Miss one and the rest of the week reshuffles, keeping a rest day between sessions where possible, and tells you what rolls into next week.
- [x] **Muscle recovery map.** Front/back body diagram plus a list with estimated readiness per muscle group from the last 7 days of sets, effort ratings and soreness check-ins. Clearly labeled as an estimate. The plan warns when a routine targets under-recovered muscles and suggests a better one.

## Onboarding ✅

- [x] **Guided setup** for new users (units, experience, goal, equipment, days, session length).
- [x] **Plan builder:** suggested split or custom days; add, swap, remove and reorder exercises before training starts. Can be redone from Settings without losing history.

## Phase 4: Hands-free ✅ (with one platform limit)

- [x] **Voice commands.** Tap the microphone during a workout and say "done", "what's next", "skip rest", "heavier", "lighter", "135 pounds", "10 reps", "easy / good / hard", "swap", "undo" or "stop". Note: most phone browsers send speech to an online recognizer, so voice *commands* may need a connection. Everything else, including the spoken voice coach, works offline.
- [ ] **Watch controls: not possible in a web app.** Browsers can't run on Wear OS or watchOS. This needs a separate native companion app (Kotlin for Wear OS, Swift for watchOS) talking to a native phone app. The data model here (one JSON log) is ready to share with one if that's built later.

---

### Design rules

1. Offline first. Everything works with no signal.
2. Explain every change. No silent weight jumps.
3. One-tap logging during the workout. Typing is optional.
4. Safety over speed: repeat or reduce when form breaks down; never push through misses forever.
5. Estimates are labeled as estimates.
6. Your data stays on your device, with a text backup you control.
