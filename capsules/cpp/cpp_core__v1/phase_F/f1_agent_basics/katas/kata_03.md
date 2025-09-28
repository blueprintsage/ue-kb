---
title: F1/k3 — Flee, Pursuit & Evasion
kit_id: f1_agent_basics
version: 1.0
status: Draft
type: kata
---
## Objective
Implement **Flee** and predictive **Pursuit/Evasion** using target relative velocity.
## Task
Estimate intercept time via projected distance/maxSpeed; steer accordingly; cap prediction horizon.
## Acceptance
- [ ] Pursuit reduces distance faster than Seek on moving target.
- [ ] Evasion increases separation under same constraints.