# Workout Creator

A single-file workout planner and tracker. Open `index.html` in any browser (desktop or phone). There's nothing to install.

## Planning
- Add, rename, copy and delete days; drag the ≡ handle to reorder days and exercises (works with touch)
- Minimize days (tap the day name) or use Collapse all / Expand all to cut down on scrolling
- Exercise library of 150+ exercises grouped by Push / Pull / Legs / Core / Cardio and body part.
  Tap to add (tap again to undo); filter by Recent, group or search (optional)
- Swap an exercise for an alternative that works the same muscle group
- Per exercise: target sets, rep range (e.g. 3 × 8–12), and effort (RIR or RPE)
- Each exercise tracks **weight × reps**, **reps only** (bodyweight moves like hanging leg raises) or **time**
  (holds and cardio like planks or the treadmill). Library exercises start with a sensible choice; change it under "Tracks"

## Training
- Tap an exercise to open it, enter weight × reps for each set and tick ✓ as you go.
  Ticking an empty set fills in last session's numbers
- "Last: 185 × 8, 8, 7" shows your previous session next to each exercise
- Progressive overload hint when you hit the top of your rep range on every set
- Personal records are flagged automatically (best estimated one-rep max, most reps for bodyweight moves, longest time for holds)
- "Finish workout" saves the ticked sets to the **Workout Log**
- **Rest timer** pinned to the bottom of the screen (30s / 60s / 90s / 2m), with a beep and a vibration on phones

## Other
- **Bodyweight log** with change over time
- **Backup reminder** if you haven't exported a backup in 7 days
- Phone-friendly "training notebook" design with colour-coded muscle groups (Push red, Pull navy, Legs olive, Core maroon) and a dark mode
- **This week** summary: days trained, sets, PRs and your last workout
- Saves automatically in your browser. Export/Import a `.json` file for backups or to move between devices
  (older backup files still import)

## Versioning

The version is shown at the bottom of the page and set by `APP_VERSION` in `index.html`.
It starts at 1.1 and goes up by 0.1 with each update (1.1, 1.2, 1.3, ...).
