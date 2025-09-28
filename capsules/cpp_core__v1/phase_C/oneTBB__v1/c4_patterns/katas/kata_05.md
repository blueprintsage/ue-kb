---
title: C4/k5 — fan-in barrier
kit_id: c4_patterns
version: 1.0
status: Draft
type: kata
---
## Goal
Merge multiple streams safely.
## Task
Use Flow Graph `continue_node` as barrier; assert final count.
## Acceptance
- [ ] All branches accounted; no deadlocks