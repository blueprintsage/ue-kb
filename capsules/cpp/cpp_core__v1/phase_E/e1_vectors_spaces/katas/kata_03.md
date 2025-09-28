---
title: E1/k3 — Projection & Rejection
kit_id: e1_vectors_spaces
version: 1.0
status: Draft
type: kata
---

## Objective
Decompose vector `v` into components parallel and orthogonal to unit normal `n`.

## Task
`v∥ = dot(v,n)*n`, `v⊥ = v − v∥`; verify `v = v∥ + v⊥` and `dot(v⊥,n)=0`.

## Acceptance
- [ ] Reconstruction error < 1e-7.
- [ ] Orthogonality within 1e-7.

## Keep/Revert
KEEP: normalize `n` with epsilon check. REVERT: assume `n` is unit.