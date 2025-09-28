---
title: E4/k12 — ULP Distance Comparator
kit_id: e4_numerics_stability
version: 1.0
status: Draft
type: kata
---
## Objective
Measure equality by **Units in the Last Place** for floats.
## Task
Implement `ulps_equal(a,b,maxUlps)` using integer reinterpretation; test vs nearly_equal on corner cases (±0, subnormals, infinities, NaN handling policy).
## Acceptance
- [ ] Passes IEEE edge cases; NaNs compare false; ±0 compares equal.
- [ ] ulps_equal agrees with nearly_equal on typical ranges.
## Keep/Revert
KEEP: sign-aware integer distance. REVERT: treat NaN as equal.