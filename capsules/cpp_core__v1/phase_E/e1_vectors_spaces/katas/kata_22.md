---
title: E1/k22 — Plane Projection Matrix
kit_id: e1_vectors_spaces
version: 1.0
status: Draft
type: kata
---
## Objective
Construct the 3×3 matrix `P = I − nn^T` that projects any vector onto a plane with unit normal `n`.
## Task
Given unit `n`, compute `P` and test `P n = 0`, `P^2 = P`, and `P^T = P`.
## Acceptance
- [ ] Idempotent and symmetric within 1e‑6.
- [ ] `‖P x‖ ≤ ‖x‖` and `dot(Px,n)=0` for random `x`.
## Keep/Revert
KEEP: normalize `n`. REVERT: unnormalized normal causing scale error.