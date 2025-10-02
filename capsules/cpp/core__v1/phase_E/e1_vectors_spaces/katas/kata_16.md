---
title: E1/k16 — Angles Between Lines & Planes
kit_id: e1_vectors_spaces
version: 1.0
status: Draft
type: kata
---
## Objective
Compute angle between two 3D lines and between two planes.
## Task
Line angle: acos( |u·v| ). Plane angle: acos( |n1·n2| ). Use unit directions.
## Acceptance
- [ ] Values match constructed test cases within 1e‑6.
- [ ] Parallel/perpendicular cases return 0/π/2 respectively.
## Keep/Revert
KEEP: absolute dot to get acute angle. REVERT: raw acos causing obtuse when not wanted.