# Decisions

Dated record of architecture/design choices and the reasoning behind them.

## 2026-07-29 — Abstract classes ahead of the course
Tower and Enemy will be abstract base classes even though part06 (abstract classes)
hasn't been covered yet in MOOC.fi. Concepts explained as needed, at a slower,
visual pace.

## 2026-07-29 — Frontend/backend bridge: JavaFX WebView
Backend stays pure vanilla Java (no framework). Frontend is HTML/CSS/JS, vibe-coded,
embedded in the Java app via JavaFX's WebView component. Java pushes game state to
the JS side each tick via WebEngine.executeScript(...). No server, no networking layer.

## 2026-07-29 — Folder scheme vs. Maven convention
Maven requires real source under src/main/java/com/ironhold/... — that stays as-is.
Plans/, Backend/, Frontend/, UI/, Characters/ are organizational folders (docs,
notes, mockups, asset planning) layered on top, not alternate source roots.

## 2026-07-29 — Art strategy
No 3D models needed (2D game). Start with free/CC0 tower-defense sprite packs
(e.g. Kenney.nl) as placeholders so art never blocks a programming milestone.
Swap in nicer art during the polish pass (milestone 4).

## 2026-07-29 — Backend ownership split
Backend stays ~90-95% hand-coded by Ellison, on purpose, to build the learning
habit — Claude assists only when genuinely stuck. Claude Code is used mainly for
frontend design work, not backend logic.

## 2026-07-29 — Claude Code attribution config
Added .claude/settings.json (attribution.commit / attribution.pr set to "") at the
repo root, same pattern used on RetainIQ, so Claude Code doesn't appear as a
contributor in git history / GitHub's contributor graph. Applies repo-wide.
