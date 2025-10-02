---
title: C1/k3 — arena concurrency
kit_id: c1_tasks_arenas
version: 1.0
status: Draft
type: kata
---
## Goal
Compare arenas sized 1 vs default.
## Task
Measure throughput of the same workload; assert Arena(1) ≈ serial.
## Acceptance
- [ ] Timing shows expected scaling.