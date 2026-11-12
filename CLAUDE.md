# Notes for Claude

- The app is a single file: `index.html` (plain HTML/CSS/JS, no build step). Styling uses CSS variables with a light and a dark theme; keep both themes working and keep it phone-friendly.
- Design (since 2.1): "training notebook" look with the user's palette only: maroon `#630C00`, navy `#002763`, olive `#4A6300`, red `#B81700` (plus warm paper/ink neutrals; dark mode uses lighter tints of the same colours). Muscle groups are colour-coded: Push = red, Pull = navy, Legs = olive, Core = maroon, Cardio = striped maroon. Headings use Barlow Condensed, body text Barlow (Google Fonts, with system fallbacks).
- Every change to the app must bump `APP_VERSION` in `index.html` by 0.1 (1.1 -> 1.2 -> 1.3 ...).
- Data is stored in localStorage under `workoutPlan`, `workoutLog`, `workoutBodyweight`, `workoutSettings` and `workoutTheme`. Everything loaded or imported goes through the `clean*` functions; keep import working for older export files (1.0 plain arrays, and pre-1.7 logs/plans that used single `sets`/`reps`/`weight` numbers).
- Exercises have a tracking `type`: `weight` (weight × reps), `reps` (bodyweight, no weight box) or `time` (holds/cardio, stored in seconds). Defaults come from `TIME_EXERCISES` / `REPS_EXERCISES`; add new library exercises to those lists when they aren't weighted.
- The user doesn't want to type to add exercises: adding must work by tapping (search is optional only).
- The site is published with GitHub Pages; `.nojekyll` tells Pages to serve the files as-is.
