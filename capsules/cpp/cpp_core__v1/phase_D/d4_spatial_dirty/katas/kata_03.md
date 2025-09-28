---
title: D4/k3 — Dirty flag cache
kit_id: d4_spatial_dirty
version: 1.0
status: Draft
type: kata
---
## Goal
Cache AABB; recompute only when position/size changes.
## Task
Mark dirty on setters; recompute lazily.
## Acceptance
- [ ] No recompute on reads when not dirty.