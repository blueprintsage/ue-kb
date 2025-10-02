---
title: F1/k16 — Formation: Offset Pursuit (Slots)
kit_id: f1_agent_basics
version: 1.0
status: Draft
type: kata
---
## Objective
Maintain a formation around a moving leader using fixed local offsets (slots).
## Task
Transform slot offsets by leader pose; pursue that moving target with arrive; reassign slots on joins/leaves.
## Acceptance
- [ ] Max slot error ≤ tolerance under turns/accelerations.
- [ ] Reassignment has ≤1 frame of double‑occupancy.