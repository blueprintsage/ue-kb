---
title: E1/k8 — Reflection Across a Normal
kit_id: e1_vectors_spaces
version: 1.0
status: Draft
type: kata
---

## Objective
Reflect vector v about unit normal n: `r = v − 2*dot(v,n)*n`.

## Task
Implement reflect; verify incident angle equals reflection angle.

## Acceptance
- [ ] `‖v‖ == ‖r‖` when n is unit (within epsilon).
- [ ] Angle of incidence = angle of reflection within 1e‑6.

## Keep/Revert
KEEP: normalize n; clamp dot. REVERT: un‑normalized normals.