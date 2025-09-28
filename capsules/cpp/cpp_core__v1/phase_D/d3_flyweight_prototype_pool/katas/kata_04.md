---
title: D3/k4 — Pooled vs naive
kit_id: d3_flyweight_prototype_pool
version: 1.0
status: Draft
type: kata
---
## Goal
Compare spawn/despawn time.
## Task
Time creating/destroying 10k objects pooled vs new/delete.
## Acceptance
- [ ] Pooled path faster / fewer allocations.