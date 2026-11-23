# Notes for Claude

- The whole app is `index.html`. Keep it a single self-contained file (no build tools, no external JS except Google Fonts).
- The user mostly uses it on an iPhone in dark mode: check changes at ~390px width in both light and dark themes.
- Keep the climbing-wall look: board background with bolt holes, screws on cards, holds as active buttons, bolts for empty/off states.
- Diagrams are drawn by the figure engine from joint angles; edit poses in `EXD`, not hand-drawn SVG.
- Workouts must not go to failure; progression raises a target only when every set hits it in a Full session.
- Bump `<meta name="crux-version">` in `index.html` with every change that ships (patch for fixes, minor for features, major for redesigns). The header shows it.
