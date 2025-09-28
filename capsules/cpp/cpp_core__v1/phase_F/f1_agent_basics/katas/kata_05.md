---
title: F1/k5 — Obstacle Avoidance (Raycasts)
kit_id: f1_agent_basics
version: 1.0
status: Draft
type: kata
---
## Objective
Steer to avoid obstacles using forward/side whisker raycasts and a lateral avoidance force.
## Task
Cast rays; if hit within lookahead, compute steer away along surface normal or choose bypass side.
## Acceptance
- [ ] Zero collisions on randomized obstacle course (≤N agents).
- [ ] No oscillation in narrow corridors (hysteresis or cooldown).