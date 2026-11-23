# Crux — strength log

A single-page workout tracker for climbing strength: bodyweight and pull-up bar training with automatic progression, quick/full sessions, max tests, progress charts, and interactive form diagrams.

Everything lives in `index.html` (HTML, CSS and JS in one file, no build step).

## Run it
Open `index.html` in a browser. Data is saved in the browser (localStorage). When the page runs as a Claude artifact it also syncs to the user's Claude account.

## Main parts of `index.html`
- **Theme**: CSS variables at the top of the first `<style>`; the climbing-wall theme (board, holds, bolts) is the second `<style>` block.
- **Storage**: `persist()` / `boot()`.
- **Figure engine**: `/* ===== Figure engine v2` — joint-angle poses (`sidePose`, `frontPose`), `drawSide`, `drawFront`.
- **Exercise library**: `EXD` — poses, captions, cues, mistakes, steps per exercise.
- **Diagram viewer**: `stageSVG`, `gripGuide`, `viewerInner`, `bindViewers`.
- **Views**: `vToday`, `vProgress`, `vHistory`, `vPlan`.
