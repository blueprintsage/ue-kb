---
title: BR17/k1 — Seeded RNG wrapper
kit_id: br17_procgen
version: 1.0
status: Draft
type: kata
---
## Goal
Deterministic random numbers from a seed.
## Task
Make a BP function `RandFromSeed(seed, index)` using `RandomStream`.
## Acceptance
- [ ] Same seed/index → same value across runs.