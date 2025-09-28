---
title: E2/k24 — TRS Interpolation (slerp/lerp)
kit_id: e2_transforms
version: 1.0
status: Draft
type: kata
---
## Objective
Interpolate between two transforms by slerping rotation and lerping translation/scale; keep rotation orthonormal.
## Task
Given (T0,R0,S0) and (T1,R1,S1), compute T(t)=lerp, R(t)=slerp (shortest arc), S(t)=lerp. Build M(t) and test properties.
## Acceptance
- [ ] Endpoints exact; R(t) unit length; det>0.
- [ ] Path monotone for T,S; rotation angle progresses smoothly.
## Keep/Revert
KEEP: shortest‑arc flip for quats; re‑normalize. REVERT: naive lerp of quaternion components (shrinks).