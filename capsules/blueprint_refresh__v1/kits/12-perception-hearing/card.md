---
title: BR12 — Perception/Hearing & Investigation
kit_id: br12_perception_hearing
version: 1.0
status: Draft
category: Blueprint
deliverables:
demo_map: BR12_BT_Map
media:
- type: screenshot
views: [TOP, BEAUTY]
assets: []
dependencies: [br06_bt_chase]
---


## Objective
Upgrade PawnSensing to AIPerception with hearing; generate a noise on shots to lure AI.


## Steps
1) Add `AIPerception` to AI; sight + hearing senses.
2) Player: when firing, call `ReportNoiseEvent`.
3) BT: On hearing, set `LastKnownLocation` and investigate.


## Acceptance
- [ ] AI reacts to noise out of sight.
- [ ] Returns to patrol if nothing found.