---
title: E3/k22 — OBB–Plane Classification & Distance
kit_id: e3_geometry_collision
version: 1.0
status: Draft
type: kata
---
## Objective
Classify an oriented box against a plane and compute signed distance bounds.
## Task
Let plane (n,d), OBB center c, axes a_i, half-extents e_i. Compute r = Σ e_i |n·a_i|; s = n·c − d. Box is in front if s−r>0, behind if s+r<0, else intersect.
## Acceptance
- [ ] Matches brute-force vertex classification across random OBBs.
- [ ] r bound ≥ max |n·(vertex−c)| within ε.
## Keep/Revert
KEEP: absolute dot extents sum. REVERT: test only c vs plane.