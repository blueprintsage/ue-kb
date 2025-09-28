---
title: E3/k8 — AABB Overlap & Sweep (1D→3D)
kit_id: e3_geometry_collision
version: 1.0
status: Draft
type: kata
---
## Objective
Test static AABB overlap and extend to swept (dynamic) overlap in one dimension, then apply per-axis.
## Task
Static: intervals [a0,a1] vs [b0,b1]. Dynamic: relative velocity v; compute entry/exit times. Lift to 3D by AND-ing per axis.
## Acceptance
- [ ] Static test matches slab overlap.  
- [ ] Sweep returns entry≤exit and detects no-hit properly.
## Keep/Revert
KEEP: open/closed interval policy consistent. REVERT: off-by-one with inclusive bounds.