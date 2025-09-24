---
title: BR08/k1 — Input mode & focus sanity
kit_id: br08_menus_pause
version: 1.0
status: Draft
type: kata
---
## Goal
Ensure correct input mode and UI focus when pausing/resuming.
## Given
Title map, Game map, WBP_Pause.
## Task
On pause: `Set Game Paused true` + `Set Input Mode UI Only` targeting WBP_Pause; on resume: `Set Game Paused false` + `Set Input Mode Game Only`.
## Acceptance
- [ ] Arrow/WASD don’t move while paused.
- [ ] After Resume, character moves and UI loses focus.