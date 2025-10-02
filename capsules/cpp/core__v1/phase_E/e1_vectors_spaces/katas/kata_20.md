---
title: E1/k20 — 2D Oriented Angle (atan2 of cross/dot)
kit_id: e1_vectors_spaces
version: 1.0
status: Draft
type: kata
---
## Objective
Compute signed angle from vector a to b in 2D using atan2(cross, dot).
## Task
θ = atan2( a×b, a·b ) returning (−π,π]; cross = a.x*b.y − a.y*b.x.
## Acceptance
- [ ] θ positive for CCW rotation, negative for CW.
- [ ] Robust near 0 and π; clamp inputs.
## Keep/Revert
KEEP: atan2(cross,dot) form. REVERT: acos(dot) losing sign.