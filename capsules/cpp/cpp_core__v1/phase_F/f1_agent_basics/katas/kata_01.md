---
title: F1/k1 — Agent Update Loop (Stable Integrator)
kit_id: f1_agent_basics
version: 1.0
status: Draft
type: kata
---
## Objective
Implement a frame update: accumulate steering → clamp accel/vel → semi-implicit integrate → clear frame forces.
## Task
Given maxAccel, maxSpeed, dt, update position/velocity with clamped acceleration; ensure deterministic results for fixed seed.
## Acceptance
- [ ] Speed never exceeds maxSpeed+ε; energy bounded on zero input.
- [ ] Identical seeds produce identical trajectories.