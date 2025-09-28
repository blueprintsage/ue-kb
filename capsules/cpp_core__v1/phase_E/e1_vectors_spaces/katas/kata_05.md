---
title: E1/k5 — Scalar Triple & Volume Sign
kit_id: e1_vectors_spaces
version: 1.0
status: Draft
type: kata
---

## Objective
Compute signed volume of parallelepiped to test orientation.

## Task
`V = dot(a, cross(b,c))`; verify sign flips on swapping two vectors.

## Acceptance
- [ ] `V(a,b,c) = −V(b,a,c)` and equals 6×tetrahedron volume.
- [ ] Near‑coplanar cases stable within epsilon.

## Keep/Revert
KEEP: use double internally if floats. REVERT: float‑only on ill‑conditioned sets.