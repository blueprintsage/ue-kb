kata_02.md---
title: BR01/k2 — Add/Remove HUD cleanly
kit_id: br01_umg_hud_basics
version: 1.0
status: Draft
type: kata
---
## Goal
Ensure no widget leak on level transition.
## Task
Remove widget on `EndPlay` (or when player dies).
## Acceptance
- [ ] After level change, no duplicate widgets are present.