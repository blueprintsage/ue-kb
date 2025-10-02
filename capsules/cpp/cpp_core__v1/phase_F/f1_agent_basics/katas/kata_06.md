---
title: F1/k6 — Boids: Separation/Alignment/Cohesion
kit_id: f1_agent_basics
version: 1.0
status: Draft
type: kata
---
## Objective
Compute local flocking forces with neighborhood queries.
## Task
Within radius r, separation = sum away inversely weighted by distance; alignment = avg neighbor velocity; cohesion = steer to centroid.
## Acceptance
- [ ] Flock maintains spacing without collapse; tunable via weights.
- [ ] O(N log N) with spatial grid (vs O(N²)).