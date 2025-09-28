---
title: C2/k6 — limiter back-pressure
kit_id: c2_flow_graph
version: 1.0
status: Draft
type: kata
---
## Goal
Hold at most K in‑flight items.
## Task
Place `limiter_node(K)` before work; decrement tokens at sink.
## Acceptance
- [ ] Peak in‑flight equals K; throughput stable.