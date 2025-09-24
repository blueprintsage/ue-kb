---
title: BR10 — Spawning & Waves
kit_id: br10_spawning_waves
version: 1.0
status: Draft
category: Blueprint
deliverables:
demo_map: BR10_Spawn_Map
media:
- type: screenshot
views: [TOP, BEAUTY]
assets: []
dependencies: []
---


## Objective
Create a simple spawner that emits N enemies per wave with a cooldown and end-of-wave event.


## Steps
1) Place `TargetPoint` array for spawn locations.
2) `StartWave(N, Rate)`: spawn on timer until N; track alive count.
3) When alive hits zero, broadcast `OnWaveCleared`.


## Acceptance
- [ ] Correct count spawned; wave ends when all dead.
- [ ] Next wave waits for cooldown.