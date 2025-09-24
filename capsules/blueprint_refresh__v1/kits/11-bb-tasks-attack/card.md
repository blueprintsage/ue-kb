---
title: BR11 — Blackboard Tasks: Attack/Investigate
kit_id: br11_bb_attack_investigate
version: 1.0
status: Draft
category: Blueprint
deliverables:
demo_map: BR11_BT_Map
media:
- type: screenshot
views: [TOP, BEAUTY]
assets: []
dependencies: [br05_bt_patrol]
---


## Objective
Add BT tasks for melee attack when in range; investigate last known location when target lost.


## Steps
1) Blackboard: `TargetActor`, `LastKnownLocation` (Vector).
2) Task_Attack: check range; play montage; cooldown.
3) Task_Investigate: move to `LastKnownLocation`, wait, clear.


## Acceptance
- [ ] Attack triggers only in range and respects cooldown.
- [ ] Investigate fires after loss and returns to patrol.