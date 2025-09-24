---
title: BR10/k1 — Timer-driven spawn loop
kit_id: br10_spawning_waves
version: 1.0
status: Draft
type: kata
---
## Goal
Spawn N enemies at Rate using a repeating timer.
## Given
Array of TargetPoints.
## Task
`StartWave(N, Rate)`: set counter=0; timer every `1/Rate` → Spawn at next point; ++counter; clear timer when counter==N.
## Acceptance
- [ ] Exactly N spawns per StartWave call.
- [ ] Timer clears after final spawn.