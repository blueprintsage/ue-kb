---
title: E4/k5 — Lerp Precision & FMA
kit_id: e4_numerics_stability
version: 1.0
status: Draft
type: kata
---
## Objective
Compare `lerp(a,b,t)` implementations and FMA effects near t≈0/1.
## Task
Implement `a + t*(b-a)` and `std::lerp` (C++20); test errors for extreme a,b and tiny t; optionally use `std::fma` path.
## Acceptance
- [ ] `std::lerp` or FMA form shows lower max error near endpoints.
- [ ] Monotonicity preserved for t∈[0,1].
## Keep/Revert
KEEP: prefer `std::lerp`/FMA. REVERT: `(1-t)*a + t*b` (can overflow/underflow).