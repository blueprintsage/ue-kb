---
title: BR06 — Behavior Trees II: Patrol → Chase
kit_id: br06_bt_chase
version: 1.0
status: Draft
category: Blueprint
deliverables:
demo_map: BR06_BT_Map
media:
- type: screenshot
views: [TOP, BEAUTY]
assets: []
dependencies: [br05_bt_patrol]
---


## Objective
Extend patrol with a simple chase on sight using Pawn Sensing.


## Setup
- Add `PawnSensing` to AI pawn; Sight radius 1500, FoV 70°.
- Blackboard: add `TargetActor` (Object).


## Steps
1) On `OnSeePawn`, set `TargetActor`; on lost (timer), clear it.
2) BT: Selector [Chase, Patrol].
- **Chase:** `MoveTo(TargetActor)` until lost.
- **Patrol:** as BR05.


## Acceptance
- [ ] AI switches from patrol to chase when player enters sight.
- [ ] Returns to patrol within 1s after losing sight.


## Keep/Revert
KEEP: PawnSensing for simplicity.
REVERT: Upgrade to AIPerception later.