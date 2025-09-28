---
title: E4/k1 — Epsilon Equality (abs + rel)
kit_id: e4_numerics_stability
version: 1.0
status: Draft
type: kata
---
## Objective
Implement robust float comparisons using absolute and relative tolerances.
## Task
Write `bool nearly_equal(a,b,abs_eps,rel_eps)` that returns true if `|a-b| ≤ max(abs_eps, rel_eps*max(|a|,|b|))`.
## Acceptance
- [ ] Passes edge cases: large magnitudes, tiny numbers near 0, opposite signs.
- [ ] Unit tests cover 1e-8..1e-3 ranges; no false positives on widely separated values.
## Keep/Revert
KEEP: combined abs/rel check. REVERT: single fixed epsilon for all scales.