---
title: E1/k21 — Householder Align (v → +Z)
kit_id: e1_vectors_spaces
version: 1.0
status: Draft
type: kata
---
## Objective
Build a **Householder reflection** that maps a unit vector `v` to the +Z axis, then verify it’s orthogonal and involutory.
## Task
Let `e = (0,0,1)`. If `v≈−e`, pick `e=(0,1,0)` instead. Compute `u = normalize(v−e)`, `H = I − 2 uu^T`. Check `H v = e`.
## Acceptance
- [ ] `H` orthogonal (`H^T H = I` within 1e‑6) and `H^2 ≈ I`.
- [ ] Works for `v` near ±Z with fallback branch.
## Keep/Revert
KEEP: fallback when `‖v−e‖` small. REVERT: divide by ~0 when `v≈e`.