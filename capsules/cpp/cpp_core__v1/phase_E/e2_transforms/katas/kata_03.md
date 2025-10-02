---
title: E2/k3 — LookAt Matrix
kit_id: e2_transforms
version: 1.0
status: Draft
type: kata
---
## Objective
Construct a right‑handed LookAt view matrix from eye, target, and up.
## Task
Compute forward = normalize(target−eye); right = normalize(cross(up,forward)); up' = cross(forward,right). Build view.
## Acceptance
- [ ] Orthonormal basis within 1e‑6; view*eye = (0,0,0,1).
- [ ] Gimbal case handled when up ≈ forward (choose fallback up).
## Keep/Revert
KEEP: re‑orthonormalize up'. REVERT: assume input up is orthogonal.