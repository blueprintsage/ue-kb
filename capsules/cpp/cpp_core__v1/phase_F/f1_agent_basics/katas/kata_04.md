---
title: F1/k4 — Wander (Jittered Target on Circle)
kit_id: f1_agent_basics
version: 1.0
status: Draft
type: kata
---
## Objective
Generate natural wandering by jittering a target on a forward-projected circle.
## Task
Maintain wanderAngle; each step add small noise; project circle ahead; seek that point.
## Acceptance
- [ ] Path curvature bounded; no sharp turns beyond limit.
- [ ] Statistical properties stable over long runs (mean turn rate).