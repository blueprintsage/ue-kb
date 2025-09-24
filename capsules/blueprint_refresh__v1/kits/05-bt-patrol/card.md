---
title: BR05 — Behavior Trees I: Patrol
kit_id: br05_bt_patrol
version: 1.0
status: Draft
category: Blueprint
deliverables:
demo_map: BR05_BT_Map
media:
- type: screenshot
views: [TOP, BEAUTY]
assets: []
dependencies: []
---


## Objective
Get an AI pawn patrolling between three points using Behavior Tree + Blackboard.


## Setup
- Add `NavMeshBoundsVolume` covering patrol area.
- Create `AIController_BP` and set as AI Pawn controller.
- Blackboard keys: `PatrolIndex` (int), `PatrolPoints` (array of Vector).


## Steps
1) Place three `TargetPoint` actors; record their locations into `PatrolPoints` at BeginPlay.
2) Behavior Tree: Sequence → Task `MoveTo`(current point) → Task `SetNextIndex` → Wait(0.5s) → Loop.
3) In `SetNextIndex` task (BP), increment and wrap `PatrolIndex`.


## Acceptance
- [ ] Pawn loops through all three points and repeats.
- [ ] Works after reloading level (no missing keys).


## Keep/Revert
KEEP: Simple vector array approach.
REVERT: Swap to actor references if you prefer.