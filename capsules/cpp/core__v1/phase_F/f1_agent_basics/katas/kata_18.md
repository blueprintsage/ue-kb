---
title: F1/k18 — Velocity Matching (Align Speeds)
kit_id: f1_agent_basics
version: 1.0
status: Draft
type: kata
---
## Objective
Match velocity with local neighbors to reduce shear and turbulence.
## Task
Compute desired vel = average neighbor velocity; steer toward it with gain and clamp.
## Acceptance
- [ ] Group average relative speed drops below threshold.
- [ ] Does not stall agents (maintains min progress toward goal).