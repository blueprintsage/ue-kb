---
title: E2/k20 — Swing‑Twist Clamp (Quat Limits)
kit_id: e2_transforms
version: 1.0
status: Draft
type: kata
---
## Objective
Limit a quaternion by decomposing into twist (around axis) and swing (off‑axis) and clamping each.
## Task
Given joint axis ẑ, decompose q into q_twist * q_swing; clamp twist angle and swing cone; recompose.
## Acceptance
- [ ] Clamped rotation stays inside limits; continuity across limits.
- [ ] Identity when limits are wide.
## Keep/Revert
KEEP: normalize at each step; shortest‑arc choices. REVERT: Euler clamp (gimbal risk).