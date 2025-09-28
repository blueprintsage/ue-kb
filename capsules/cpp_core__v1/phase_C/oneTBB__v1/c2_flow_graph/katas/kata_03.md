---
title: C2/k3 — buffer decoupling
kit_id: c2_flow_graph
version: 1.0
status: Draft
type: kata
---
## Goal
Insert `buffer_node` to decouple rates.
## Task
Producer bursts; consumer sleeps; assert no drops and eventual completion.
## Acceptance
- [ ] All items processed; no busy‑wait on producer.