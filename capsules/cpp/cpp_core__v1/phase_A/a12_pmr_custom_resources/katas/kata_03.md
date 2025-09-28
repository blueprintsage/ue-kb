---
title: A12/k3 — custom memory_resource stats
kit_id: a12_pmr_custom_resources
version: 1.0
status: Draft
type: kata
---
## Goal
Count bytes/allocs by deriving from pmr::memory_resource.
## Task
Override do_allocate/deallocate; forward to upstream; expose counters.
## Acceptance
- [ ] Counters match expected after pushes/clears.