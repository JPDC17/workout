# Notes for Claude

- The app is a single file: `index.html` (plain HTML/CSS/JS, no build step). Keep the styling fairly basic. Styling uses CSS variables with a light and a dark theme; keep both themes working and keep it phone-friendly.
- Only use purple tones for colour (no reds, greens, oranges, etc.).
- Every change to the app must bump `APP_VERSION` in `index.html` by 0.1 (1.1 -> 1.2 -> 1.3 ...).
- Data is stored in localStorage under `workoutPlan`, `workoutLog`, `workoutBodyweight`, `workoutSettings` and `workoutTheme`. Everything loaded or imported goes through the `clean*` functions; keep import working for older export files (1.0 plain arrays, and pre-1.7 logs/plans that used single `sets`/`reps`/`weight` numbers).
- Exercises have a tracking `type`: `weight` (weight × reps), `reps` (bodyweight, no weight box) or `time` (holds/cardio, stored in seconds). Defaults come from `TIME_EXERCISES` / `REPS_EXERCISES`; add new library exercises to those lists when they aren't weighted.
- The user doesn't want to type to add exercises: adding must work by tapping (search is optional only).
- The site is published with GitHub Pages; `.nojekyll` tells Pages to serve the files as-is.
