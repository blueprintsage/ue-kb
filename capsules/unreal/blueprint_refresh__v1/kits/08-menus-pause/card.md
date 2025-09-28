---
title: BR08 — Menus & Pause Flow
kit_id: br08_menus_pause
version: 1.0
status: Draft
category: Blueprint
deliverables:
demo_map: BR08_Menu_Map
media:
- type: screenshot
views: [BEAUTY]
assets: []
dependencies: [br04_savegame_loop]
---


## Objective
Main menu → gameplay → pause → resume with proper input modes and focus.


## Steps
1) Title map with `WBP_Title` (Play/Quit). On Play, open `Game_Map`.
2) In `Game_Map`, Esc toggles `WBP_Pause` and sets input/UI focus.
3) From Pause, Resume or return to Title.


## Acceptance
- [ ] No input leaks after resume.
- [ ] Title → Game → Pause → Resume loop works reliably.