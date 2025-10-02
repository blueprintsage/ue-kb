---
title: F1/k21 — Flow‑Field Following (Vector Grids)
kit_id: f1_agent_basics
version: 1.0
status: Draft
type: kata
---
## Objective
Follow a precomputed 2D/3D **flow field** (vector grid) with smooth steering.
## Task
Sample velocity target from the grid at agent position (bilinear/trilinear). Steer toward that velocity with a gain and clamp.
## Acceptance
- [ ] Agents converge to field directions with ≤5° heading error after τ seconds.
- [ ] Grid resolution changes do not cause oscillation (use filtered sampling).
## Keep/Revert
KEEP: filtered interpolation + maxAccel clamp. REVERT: snap desired vel to cell vector.