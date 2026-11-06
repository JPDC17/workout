# Notes for Claude

- The app is a single file: `index.html` (plain HTML/CSS/JS, no build step). Keep the styling fairly basic. Styling uses CSS variables with a light and a dark theme; keep both themes working and keep it phone-friendly.
- Only use purple tones for colour (no reds, greens, oranges, etc.).
- Every change to the app must bump `APP_VERSION` in `index.html` by 0.1 (1.1 -> 1.2 -> 1.3 ...).
- Data is stored in localStorage under `workoutPlan`, `workoutLog` and `workoutTheme`. Keep import working for older export files.
- The site is published with GitHub Pages; `.nojekyll` tells Pages to serve the files as-is.
