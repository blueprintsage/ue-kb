---
title: E4/k11 — Running Mean/Variance (Welford)
kit_id: e4_numerics_stability
version: 1.0
status: Draft
type: kata
---
## Objective
Compute mean and variance online with minimal loss of precision.
## Task
Implement Welford’s algorithm; compare to naive one-pass on adversarial sequences.
## Acceptance
- [ ] Matches batch double-precision result within 1e-10.
- [ ] No catastrophic cancellation on alternating large/small values.
## Keep/Revert
KEEP: Welford update M2. REVERT: naive (Σx²−(Σx)²/n).