---
title: B8/k19 — Small callable optimization (type erasure SBO)
kit_id: b8_perf_layout
version: 1.0
status: Draft
type: kata
---
## Objective
Implement a function wrapper with small-buffer storage.
## Acceptance
- [ ] Small callees avoid heap; large spill to heap; call overhead table included.
