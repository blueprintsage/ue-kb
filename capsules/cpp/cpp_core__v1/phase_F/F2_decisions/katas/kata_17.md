---
title: F2/k17 — Utility: Target Selection vs Action Selection
kit_id: f2_decisions
version: 1.0
status: Draft
type: kata
---
## Objective
Score **targets** (entities/locations) and **actions** jointly without combinatorial explosion.
## Task
Compute target score per entity; pick top‑K; for each, score actions; choose argmax over (target,action) pairs.
## Acceptance
- [ ] Choice matches brute‑force over all pairs but with ≤K×A evaluations.
- [ ] Stable under small noise via hysteresis.