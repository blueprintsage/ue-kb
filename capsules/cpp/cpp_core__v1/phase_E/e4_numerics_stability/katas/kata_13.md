---
title: E4/k13 — Stable exp/log/sigmoid (log1p/expm1)
kit_id: e4_numerics_stability
version: 1.0
status: Draft
type: kata
---
## Objective
Avoid overflow/underflow and cancellation in exponential/logarithmic code.
## Task
Provide wrappers using `std::expm1`, `std::log1p`, and a clamped sigmoid; verify stable outputs for |x|>20 and x≈0.
## Acceptance
- [ ] Relative error vs high-precision reference < 1e-12 near 0.
- [ ] No inf/NaN for large magnitude inputs under policy.
## Keep/Revert
KEEP: log-sum-exp trick where needed. REVERT: raw `exp`/`log` in unstable regions.