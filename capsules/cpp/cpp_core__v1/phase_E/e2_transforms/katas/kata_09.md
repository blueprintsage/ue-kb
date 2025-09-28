---
title: E2/k9 — Euler Angles Pitfalls
kit_id: e2_transforms
version: 1.0
status: Draft
type: kata
---
## Objective
Demonstrate gimbal lock and axis‑order sensitivity with Euler angles.
## Task
Convert R→(yaw,pitch,roll) under two orders; show different results; test near gimbal lock where pitch≈±90°.
## Acceptance
- [ ] Orders produce distinct triples for same R.
- [ ] Near‑lock region produces large param jumps though R is smooth.
## Keep/Revert
KEEP: document order and range. REVERT: assume unique Euler solution.