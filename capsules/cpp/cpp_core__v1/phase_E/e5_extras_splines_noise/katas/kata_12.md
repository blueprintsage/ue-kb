---
title: E5/k12 — Near-Uniform Sampling by Arc Length
kit_id: e5_extras_splines_noise
version: 1.0
status: Draft
type: kata
---
## Objective
Sample a Bezier curve at approximately equal arc-length spacing using a lookup table.
## Task
Build cumulative length table (E5/k5); invert with binary search to get M segments of equal length.
## Acceptance
- [ ] Spacing variance ≤ 5% vs ground-truth fine sampling.
- [ ] Works for both gentle and high-curvature curves.
## Keep/Revert
KEEP: binary search + local Newton refine. REVERT: uniform t samples.