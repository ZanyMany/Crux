# Notes for Claude

- The whole app is `index.html`. Keep it a single self-contained file (no build tools, no external JS except Google Fonts).
- The user mostly uses it on an iPhone in dark mode: check changes at ~390px width in both light and dark themes.
- Keep the friendly bouldering-wall look (v2): light grey textured wall with dark screw holes (dark grey wall in dark mode), light cartoon style (flat colour, bold ink outline, small offset shadow), sentence-case headings. Buttons are plain cartoon buttons; holds are decoration only (header, route topo); screw holes mark empty states. Use the tokens in `:root`.
- Diagrams are drawn by the figure engine from joint angles; edit poses in `EXD`, not hand-drawn SVG.
- Workouts must not go to failure; progression raises a target only when every set hits it in a Full session.
- Bump `<meta name="crux-version">` in `index.html` with every change that ships (patch for fixes, minor for features, major for redesigns). The header shows it.
