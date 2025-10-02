---
title: E1/k15 — Rotate Around Axis (Rodrigues)
kit_id: e1_vectors_spaces
version: 1.0
status: Draft
type: kata
---
## Objective
Rotate vector v by angle θ around unit axis u using **Rodrigues’ formula**.
## Task
Implement r = v cosθ + (u×v) sinθ + u(u·v)(1−cosθ); verify invariants.
## Acceptance
- [ ] ‖v‖≈‖r‖ when u is unit (within 1e‑6).
- [ ] For θ=0/π, results match expectation.
## Keep/Revert
KEEP: precompute sin/cos; clamp dot. REVERT: build 3×3 then multiply for every call.