---
title: A12/k6 — swap resources
kit_id: a12_pmr_custom_resources
version: 1.0
status: Draft
type: kata
---
## Goal
Hot-swap container’s resource by move.
## Task
Move pmr::vector from pool-backed to monotonic-backed; verify contents preserved.
## Acceptance
- [ ] After move, new allocations go to new resource; old resource can be reset safely.