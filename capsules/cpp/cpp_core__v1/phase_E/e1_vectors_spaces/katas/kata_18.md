---
title: E1/k18 — SLERP vs LERP on Unit Sphere
kit_id: e1_vectors_spaces
version: 1.0
status: Draft
type: kata
---
## Objective
Compare spherical linear interpolation to normalized LERP between two unit vectors.
## Task
Implement slerp(a,b,t) and nlerp=normalize(lerp(a,b,t)); measure angular error vs true great‑circle.
## Acceptance
- [ ] SLERP keeps constant angular velocity.
- [ ] NLERP small angular error but cheaper.
## Keep/Revert
KEEP: use clamped dot for acos. REVERT: naive lerp without renormalization (shrinks).