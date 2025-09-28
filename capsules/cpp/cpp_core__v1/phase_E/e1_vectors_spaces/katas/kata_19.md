---
title: E1/k19 — Great‑Circle Path Sampling
kit_id: e1_vectors_spaces
version: 1.0
status: Draft
type: kata
---
## Objective
Sample N evenly spaced directions along the great‑circle arc from a to b.
## Task
Use SLERP at t=i/(N−1); verify equal angular steps.
## Acceptance
- [ ] Δθ between consecutive samples constant within 1e‑6.
- [ ] Endpoints equal a and b.
## Keep/Revert
KEEP: handle a≈−b (ambiguous path) via fallback. REVERT: divide by zero at small angles.