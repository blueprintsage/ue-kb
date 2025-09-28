---
title: E2/k8 — SLERP (Quaternion)
kit_id: e2_transforms
version: 1.0
status: Draft
type: kata
---
## Objective
Implement spherical linear interpolation between unit quaternions with shortest‑arc handling.
## Task
Given qa,qb,t: if dot<0, negate one end; compute slerp with sin/acos form; handle small‑angle fallback to nlerp.
## Acceptance
- [ ] Constant angular velocity along arc; endpoints exact.
- [ ] Matches matrix‑interpolated vector tests within 1e‑6.
## Keep/Revert
KEEP: shortest‑arc flip. REVERT: slerp across long way (dot<0).