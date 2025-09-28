---
title: F2/k2 — Blackboard: Types, TTL, Observers
kit_id: f2_decisions
version: 1.0
status: Draft
type: kata
---
## Objective
Create a blackboard with typed entries, time-to-live (TTL), and change observers.
## Task
Set/get with expiry; observers fire on set/expire; unit test race cases.
## Acceptance
- [ ] Expired keys never read as valid.
- [ ] Observers fire exactly once per change.