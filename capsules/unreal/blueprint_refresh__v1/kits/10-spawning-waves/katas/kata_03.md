---
title: BR10/k3 — Cooldown & chaining waves
kit_id: br10_spawning_waves
version: 1.0
status: Draft
type: kata
---
## Goal
Chain waves with a cooldown.
## Task
After OnWaveCleared, start a timer (e.g., 3s) then StartWave of next size.
## Acceptance
- [ ] No overlap: next wave never begins before cooldown.