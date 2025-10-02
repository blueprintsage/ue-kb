---
title: E4/k7 — Explicit Euler Stability (Damped Spring)
kit_id: e4_numerics_stability
version: 1.0
status: Draft
type: kata
---
## Objective
Show energy blow-up with explicit Euler beyond stability limits.
## Task
Simulate m x¨ + c x˙ + k x = 0 using explicit Euler; vary dt and measure energy drift.
## Acceptance
- [ ] For dt below bound, solution decays; above, energy diverges.
- [ ] Plot or numeric log demonstrates threshold.
## Keep/Revert
KEEP: compute energy m v²/2 + k x²/2. REVERT: judge by eyeballing only.