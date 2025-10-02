---
title: C2/k2 — broadcast fan-out
kit_id: c2_flow_graph
version: 1.0
status: Draft
type: kata
---
## Goal
Split a stream to two consumers and merge results.
## Task
`broadcast_node` → two `function_node`s; merge via atomic sum.
## Acceptance
- [ ] Combined sum equals expected.