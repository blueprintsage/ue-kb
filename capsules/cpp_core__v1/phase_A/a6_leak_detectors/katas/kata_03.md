---
title: A6/k3 — custom leak_guard
kit_id: a6_leak_detectors
version: 1.0
status: Draft
type: kata
---
## Goal
Detect allocation growth across a scope.
## Task
Implement `leak_guard g;` that snapshots global/new counts (debug only) and reports net allocations on destruction.
## Acceptance
- [ ] Failing test prints nonzero growth; passing test prints zero.