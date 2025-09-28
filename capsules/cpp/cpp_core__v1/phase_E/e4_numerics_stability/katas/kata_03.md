---
title: E4/k3 — Kahan/Neumaier Summation
kit_id: e4_numerics_stability
version: 1.0
status: Draft
type: kata
---
## Objective
Accumulate large+small numbers accurately using compensated summation.
## Task
Sum 1e6 terms: alternating large value and tiny 1e-8; compare naive sum vs Kahan and Neumaier.
## Acceptance
- [ ] Compensated sums match high-precision (long double) within 1e-10.
- [ ] Naive sum shows visible drift; report relative error.
## Keep/Revert
KEEP: carry compensation as separate variable. REVERT: accumulate into a single float.