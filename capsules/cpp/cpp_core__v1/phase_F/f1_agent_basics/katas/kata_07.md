---
title: F1/k7 — Priority & Weighted Blending
kit_id: f1_agent_basics
version: 1.0
status: Draft
type: kata
---
## Objective
Combine multiple steering behaviors using **priority** (first that exceeds ε) or **weighted** sums with truncation at maxAccel.
## Task
Implement both combiners and compare trajectories on a mixed task (seek+avoid+flock).
## Acceptance
- [ ] Priority eliminates dithering near obstacles; weighted is smooth.
- [ ] Resultant accel magnitude ≤ maxAccel always.