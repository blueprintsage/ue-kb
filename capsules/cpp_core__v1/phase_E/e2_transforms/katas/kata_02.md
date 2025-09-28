---
title: E2/k2 — Quaternion Normalize & Multiply
kit_id: e2_transforms
version: 1.0
status: Draft
type: kata
---
## Objective
Implement quaternion normalization and multiplication; verify equivalence to matrix composition on vectors.
## Task
Generate q1,q2; compute q = normalize(q2*q1). Compare q⋅v to (R2*R1)*v.
## Acceptance
- [ ] Max angular difference < 1e‑6 rad across random tests.
- [ ] ‖q‖≈1 after chained multiplies (renormalize).
## Keep/Revert
KEEP: renormalize after multiply. REVERT: drift from floating error.