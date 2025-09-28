---
title: BR15 — Gameplay Framework in BP (GameMode/State/Player)
kit_id: br15_bp_framework
version: 1.0
status: Draft
category: Blueprint
deliverables:
demo_map: BR15_Framework_Map
media:
- type: screenshot
views: [BEAUTY]
assets: []
dependencies: []
---


## Objective
Wire GameMode → spawn rules, GameState → match data, PlayerState → score, HUD → UI.


## Steps
1) Create **BP_GameMode**, **BP_GameState**, **BP_PlayerState**; set in Project Settings→Maps & Modes.
2) Move score/time to GameState; PlayerState holds per-player data.
3) HUD/UMG reads from GameState; GameMode controls spawn rules.


## Acceptance
- [ ] Data lives in correct classes; works in PIE with two players.
- [ ] UI reflects GameState updates.