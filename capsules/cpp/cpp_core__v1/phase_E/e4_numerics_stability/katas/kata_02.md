---
title: E4/k2 — Conditioning via Rescaling
kit_id: e4_numerics_stability
version: 1.0
status: Draft
type: kata
---
## Objective
Improve numerical conditioning by rescaling problem variables.
## Task
Compute `hypot(a,b)` three ways: naive sqrt(a²+b²), stable `std::hypot`, and rescaled form dividing by max(|a|,|b|).
## Acceptance
- [ ] For extreme a,b (1e-30..1e+30), stable forms agree; naive fails some.
- [ ] Document when to rescale and the effect on overflow/underflow.
## Keep/Revert
KEEP: divide by max magnitude; multiply back. REVERT: square then sum blindly.