---
title: F1/k9 — FSM: Patrol → Chase → Search
kit_id: f1_agent_basics
version: 1.0
status: Draft
type: kata
---
## Objective
Wire a 3-state finite-state machine with transitions based on perception and timers.
## Task
Patrol waypoints; on sight → Chase; on lost for T seconds → Search spiral; on timeout → Patrol.
## Acceptance
- [ ] Transition logs match design; no stuck states.
- [ ] Deterministic with fixed seed & same stimuli.