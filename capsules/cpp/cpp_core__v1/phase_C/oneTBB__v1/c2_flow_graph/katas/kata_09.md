---
title: C2/k9 — exception safety
kit_id: c2_flow_graph
version: 1.0
status: Draft
type: kata
---
## Goal
Throw inside a node and verify graph unwinds safely.
## Task
Throw on a specific input; assert state restored; subsequent run succeeds.
## Acceptance
- [ ] No leaks; next run succeeds.