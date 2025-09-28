---
title: E4/k21 — LogSumExp & Softmax (Stable)
kit_id: e4_numerics_stability
version: 1.0
status: Draft
type: kata
---
## Objective
Implement numerically stable log-sum-exp and softmax.
## Task
Given vector x, compute m=max(x); `lse = m + log(Σ exp(x_i−m))`; `softmax_i = exp(x_i−m)/Σ exp(x_j−m)`.
## Acceptance
- [ ] Matches high-precision reference for |x| up to 100.
- [ ] No overflow/underflow; probabilities sum to 1±1e−7.
## Keep/Revert
KEEP: subtract max trick. REVERT: raw exp then divide.