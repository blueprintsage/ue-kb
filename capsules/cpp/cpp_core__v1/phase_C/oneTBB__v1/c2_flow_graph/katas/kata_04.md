---
title: C2/k4 — sequencer ordering
kit_id: c2_flow_graph
version: 1.0
status: Draft
type: kata
---
## Goal
Enforce order `key(i)` with `sequencer_node`.
## Task
Shuffle inputs; verify output ordered by key.
## Acceptance
- [ ] Output strictly ordered; concurrency still >1 upstream.