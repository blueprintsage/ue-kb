---
title: B9/k6 — Barrier/latch rendezvous
kit_id: b9_concurrency
version: 1.0
status: Draft
type: kata
---
## Objective
Coordinate N threads to meet at a barrier and proceed in phases.
## Acceptance
- [ ] All threads see phase order 1→2; no stragglers or spurious wakeups.
