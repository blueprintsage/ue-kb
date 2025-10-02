---
title: E5/k20 — SQUAD (Spherical Cubic) for Quats
kit_id: e5_extras_splines_noise
version: 1.0
status: Draft
type: kata
---
## Objective
Interpolate orientations smoothly through keyframes using **SQUAD** (spherical cubic interpolation).
## Task
Compute intermediate control quats `s_i` (Shoemake); then `squad(q0,q1,s0,s1,t) = slerp( slerp(q0,q1,t), slerp(s0,s1,t), 2t(1−t) )`.
## Acceptance
- [ ] C1 continuity across segments; no sudden angular velocity jumps.
- [ ] Reduces to SLERP for 2-keyframe case.
## Keep/Revert
KEEP: shortest-arc handling for all slerps. REVERT: linear component-wise lerp on quats.