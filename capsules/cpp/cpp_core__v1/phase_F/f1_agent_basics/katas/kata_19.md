---
title: F1/k19 — Hysteresis & Deadzones (Stable Decisions)
kit_id: f1_agent_basics
version: 1.0
status: Draft
type: kata
---
## Objective
Reduce state chatter by using entry/exit thresholds and time hysteresis.
## Task
For FOV/LOS and range checks, require enter>exit thresholds and/or min dwell time before switching states.
## Acceptance
- [ ] FSM transitions drop by ≥50% in noisy scenes.
- [ ] Responsiveness remains acceptable (measured latency bounds).