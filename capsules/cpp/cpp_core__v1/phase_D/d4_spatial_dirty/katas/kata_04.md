---
title: D4/k4 — Chained flags
kit_id: d4_spatial_dirty
version: 1.0
status: Draft
type: kata
---
## Goal
Propagate dirty to dependents.
## Task
A depends on B,C; change B; ensure A recomputes; change C; recompute again.
## Acceptance
- [ ] Exactly one recompute per dependency change.