---
title: E3/k15 — Capsule–Capsule Distance (Segments + Radii)
kit_id: e3_geometry_collision
version: 1.0
status: Draft
type: kata
---
## Objective
Compute minimal distance between two capsules; detect overlap.
## Task
Use segment–segment closest points (k5) to get d; return d − (R1+R2) and contact points.
## Acceptance
- [ ] Symmetry: swapping capsules yields same distance.
- [ ] Degenerate parallel/collinear cases handled.
## Keep/Revert
KEEP: reuse robust segment–segment with clamps. REVERT: sample endpoints only.