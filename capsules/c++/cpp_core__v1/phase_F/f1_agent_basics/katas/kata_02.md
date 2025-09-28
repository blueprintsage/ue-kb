---
title: F1/k2 — Seek & Arrive
kit_id: f1_agent_basics
version: 1.0
status: Draft
type: kata
---
## Objective
Compute steering for **Seek** (toward target) and **Arrive** (speed ramps down near radius).
## Task
Seek: accel toward desired vel. Arrive: scale desired speed by distance with slow radius; stop within tolerance.
## Acceptance
- [ ] Overshoot ≤ specified bound; settle inside arrival radius.
- [ ] Continuous acceleration profile (no jump at boundary).