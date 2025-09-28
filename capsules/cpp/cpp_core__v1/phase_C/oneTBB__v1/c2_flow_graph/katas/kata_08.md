---
title: C2/k8 — cancel graph
kit_id: c2_flow_graph
version: 1.0
status: Draft
type: kata
---
## Goal
Cancel a running graph cleanly.
## Task
Start producer; after delay call `g.cancel()`; ensure sink stops and `wait_for_all()` returns.
## Acceptance
- [ ] No deadlock; all nodes finish; counters consistent.