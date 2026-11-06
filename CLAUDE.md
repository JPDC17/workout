# Notes for Claude

- The app is a single file: `index.html` (plain HTML/CSS/JS, no build step). Keep the layout and styling basic.
- Every change to the app must bump `APP_VERSION` in `index.html` by 0.1 (1.1 -> 1.2 -> 1.3 ...).
- Data is stored in localStorage under `workoutPlan` and `workoutLog`. Keep import working for older export files.
