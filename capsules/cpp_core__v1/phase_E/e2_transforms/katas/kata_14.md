---
title: E2/k14 — Build From Basis + Position
kit_id: e2_transforms
version: 1.0
status: Draft
type: kata
---
## Objective
Construct a 4×4 transform from orthonormal basis vectors and a position.
## Task
Given right/up/forward and p, build column‑major matrix; verify inverse is (R^T, −R^T p).
## Acceptance
- [ ] Inverse correctness within 1e‑6.
- [ ] Basis stays orthonormal after tiny noise correction.
## Keep/Revert
KEEP: re‑orthonormalize input basis. REVERT: trust inputs blindly.