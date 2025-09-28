---
title: B10/k5 — Allocator-aware container (propagate on move)
kit_id: b10_resources
version: 1.0
status: Draft
type: kata
---
## Objective
Design a minimal container that accepts an allocator and respects propagate traits.
## Acceptance
- [ ] `propagate_on_container_move_assignment` obeyed; state correct after move/assign; allocator used for allocations.
