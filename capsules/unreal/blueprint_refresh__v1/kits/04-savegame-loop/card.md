---
title: BR04 — SaveGame Loop (rounds, pause)
kit_id: br04_savegame_loop
version: 1.0
status: Draft
category: Blueprint
deliverables:
demo_map: BR04_Save_Map
media:
- type: screenshot
views: [BEAUTY]
assets: []
dependencies: []
---


## Objective
Implement a tiny round system with score persistence using SaveGame; include a pause menu with resume/quit.


## Setup
- Create `SG_Profile` (SaveGame) with `HighScore` (int).
- Create `WBP_Pause` with Resume/Quit buttons.


## Steps
1) On BeginPlay: Load `SG_Profile` or create default; cache `HighScore`.
2) On round end: update `HighScore` if `Score` higher; `SaveGameToSlot`.
3) Bind `Esc` to toggle pause: `Set Game Paused`, show `WBP_Pause`.
4) Resume/quit buttons unpause or open main menu map.


## Acceptance
- [ ] HighScore persists across PIE sessions.
- [ ] Pause menu toggles reliably; input mode set correctly.


## Keep/Revert
KEEP: Single-slot save simplicity.
REVERT: Expand to multi-slot later.