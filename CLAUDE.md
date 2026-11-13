# Notes for Claude

- The app is a single file: `index.html` (plain HTML/CSS/JS, no build step). Styling uses CSS variables with a light and a dark theme; keep both themes working and keep it phone-friendly.
- Design (since 2.2): construction-site look with the user's palette only: charcoal `#17191D`, construction orange `#FF9900`, safety yellow `#FFC928`, white `#FFFFFF`, steel grey `#85898F` (light-mode text greys are darker steel shades for readability). Orange and yellow are fills behind charcoal text, never text on white. Muscle groups: Push = orange, Pull = steel, Legs = yellow, Core = charcoal (white in dark mode), Cardio = hazard stripes. Headings use Barlow Condensed, body text Barlow (Google Fonts, with system fallbacks).
- Every change to the app must bump `APP_VERSION` in `index.html` by 0.1 (1.1 -> 1.2 -> 1.3 ...).
- Data is stored in localStorage under `workoutPlan`, `workoutLog`, `workoutBodyweight`, `workoutSettings` and `workoutTheme`. Everything loaded or imported goes through the `clean*` functions; keep import working for older export files (1.0 plain arrays, and pre-1.7 logs/plans that used single `sets`/`reps`/`weight` numbers).
- Exercises have a tracking `type`: `weight` (weight × reps), `reps` (bodyweight, no weight box) or `time` (holds/cardio, stored in seconds). Defaults come from `TIME_EXERCISES` / `REPS_EXERCISES`; add new library exercises to those lists when they aren't weighted.
- The user doesn't want to type to add exercises: adding must work by tapping (search is optional only).
- The site is published with GitHub Pages; `.nojekyll` tells Pages to serve the files as-is.
