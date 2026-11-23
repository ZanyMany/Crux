# Crux — strength log

A single-page workout tracker for climbing strength: bodyweight and pull-up bar training with automatic progression, quick/full sessions, max tests, progress charts, and interactive form diagrams.

Everything lives in `index.html` (HTML, CSS and JS in one file, no build step).

## Run it
Open `index.html` in a browser. Data is saved in the browser (localStorage). When the page runs as a Claude artifact it also syncs to the user's Claude account.

## Updates
Served from GitHub Pages, the app checks for a newer version of itself each time it opens (and when you return to it after 30+ minutes). If you haven't touched anything yet it reloads straight into the new version; otherwise it shows a "New version ready" bar with a Reload button. Saved data stays put. Opened as a local file it doesn't check.

The version number shows in the header (e.g. `v1.1.0`) and comes from `<meta name="crux-version">` in `index.html`. Bump it with every change you ship; after an update the app shows "Updated to vX" once so you can confirm the phone picked it up.

## Main parts of `index.html`
- **Theme**: CSS variables at the top of the first `<style>`; the climbing-wall theme (board, holds, bolts) is the second `<style>` block.
- **Storage**: `persist()` / `boot()`.
- **Figure engine**: `/* ===== Figure engine v2` — joint-angle poses (`sidePose`, `frontPose`), `drawSide`, `drawFront`.
- **Exercise library**: `EXD` — poses, captions, cues, mistakes, steps per exercise.
- **Diagram viewer**: `stageSVG`, `gripGuide`, `viewerInner`, `bindViewers`.
- **Auto-update**: the second `<script>` (`checkUpdate`).
- **Views**: `vToday`, `vProgress`, `vHistory`, `vPlan`.
