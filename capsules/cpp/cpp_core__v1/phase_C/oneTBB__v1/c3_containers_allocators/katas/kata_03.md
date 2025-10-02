---
title: C3/k3 — concurrent_queue MPMC
kit_id: c3_containers_allocators
version: 1.0
status: Draft
type: kata
---
## Goal
Multiple producers and consumers with termination signal.
## Task
Push work items; pop until poison pill; sum results.
## Acceptance
- [ ] All items processed exactly once.