---
title: E4/k23 — Pairwise Summation (Parallel‑Friendly)
kit_id: e4_numerics_stability
version: 1.0
status: Draft
type: kata
---
## Objective
Sum large arrays with **pairwise reduction** and compare error vs naive and Kahan.
## Task
Implement recursive pairwise sum; benchmark ULP error and time for N=10^6; optional OpenMP/TBB parallel tree.
## Acceptance
- [ ] Pairwise error ≪ naive and close to Kahan; speed ≥ naive.
- [ ] Parallel version matches serial within 1 ULP (determinism optional).
## Keep/Revert
KEEP: balanced tree reductions. REVERT: linear left‑fold only.