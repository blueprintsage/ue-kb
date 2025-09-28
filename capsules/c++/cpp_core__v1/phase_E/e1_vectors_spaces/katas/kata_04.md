---
title: E1/k4 — Gram–Schmidt ONB
kit_id: e1_vectors_spaces
version: 1.0
status: Draft
type: kata
---

## Objective
Build an orthonormal basis from two non‑collinear vectors.

## Task
Given `tangent` and `approxNormal`, compute `n = normalize(approxNormal)`,
`t = normalize(tangent − dot(tangent,n) n)`, `b = cross(n,t)`.

## Acceptance
- [ ] `‖n‖≈‖t‖≈‖b‖≈1` and pairwise dots < 1e-6.
- [ ] Handles near‑collinear inputs by picking a safe fallback axis.

## Keep/Revert
KEEP: fallback axis when `‖t‖` small. REVERT: divide by ~0.