---
title: E1/k24 — Mean Direction of Unit Vectors
kit_id: e1_vectors_spaces
version: 1.0
status: Draft
type: kata
---
## Objective
Compute the **mean direction** on S² by averaging and renormalizing unit vectors; report resultant length R as concentration.
## Task
Given unit set {v_i}, compute `m = normalize(Σ v_i)` and `R = ‖Σ v_i‖/N`; validate against known configurations.
## Acceptance
- [ ] For symmetric pairs (v,−v), R≈0. For identical vectors, R≈1.
- [ ] m near true direction for mildly noisy samples.
## Keep/Revert
KEEP: sum in double for stability. REVERT: single‑precision sum on large N.