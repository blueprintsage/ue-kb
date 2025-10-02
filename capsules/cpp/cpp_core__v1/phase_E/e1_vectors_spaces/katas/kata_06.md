---
title: E1/k6 — Change of Basis
kit_id: e1_vectors_spaces
version: 1.0
status: Draft
type: kata
---

## Objective
Convert coordinates between world basis and an arbitrary ONB.

## Task
Given ONB {u,v,w} (columns of R), compute local `x' = R^T (x − p)` and back `x = R x' + p`.

## Acceptance
- [ ] Round‑trip error < 1e-7 for random x, p.
- [ ] R orthonormal (R·R^T = I within epsilon).

## Keep/Revert
KEEP: precompute R^T. REVERT: invert R numerically.