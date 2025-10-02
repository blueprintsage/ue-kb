---
title: E4/k9 — Safe Normalize & Saturate
kit_id: e4_numerics_stability
version: 1.0
status: Draft
type: kata
---
## Objective
Provide safe `normalize_eps` and `saturate` helpers used across geometry.
## Task
`normalize_eps(v,eps)` returns zero when ‖v‖≤eps; `saturate(x)` clamps to [0,1]; include tests for denormals/NaNs.
## Acceptance
- [ ] No NaNs on zero input; unit length within 1e-7 for typical vectors.
- [ ] Saturate is branchless or minimal-branch and correct.
## Keep/Revert
KEEP: early-out on small norms. REVERT: blind division by norm.