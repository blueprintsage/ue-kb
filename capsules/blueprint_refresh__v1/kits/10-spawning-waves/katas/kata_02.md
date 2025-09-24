---
title: BR10/k2 — Alive-count tracking
kit_id: br10_spawning_waves
version: 1.0
status: Draft
type: kata
---
## Goal
Track live enemies accurately.
## Task
On spawn: ++Alive; on enemy death: --Alive; if Alive==0 and N spawned, fire OnWaveCleared.
## Acceptance
- [ ] OnWaveCleared only fires when the last enemy dies.