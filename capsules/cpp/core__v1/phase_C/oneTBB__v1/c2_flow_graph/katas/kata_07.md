---
title: C2/k7 — node concurrency
kit_id: c2_flow_graph
version: 1.0
status: Draft
type: kata
---
## Goal
Compare serial vs unlimited `function_node`.
## Task
Run both configs on same workload; time them.
## Acceptance
- [ ] Unlimited is faster for CPU‑bound work; serial gives deterministic order.