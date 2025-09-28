---
title: F4/k6 — Plan Execution & Monitoring (Replan Hook)
kit_id: f4_planning_learning
version: 1.0
status: Draft
type: kata
---
## Objective
Execute the action queue; when an action fails or world changes, trigger replan.
## Task
Maintain `expected_preconds`; before each step, verify; if mismatch, replan from current state; log latency.
## Acceptance
- [ ] No dead‑actions executed after world change.
- [ ] Replan latency within budget; plan recovers to goal.