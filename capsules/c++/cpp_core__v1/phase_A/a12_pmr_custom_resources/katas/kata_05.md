---
title: A12/k5 — arena adapter
kit_id: a12_pmr_custom_resources
version: 1.0
status: Draft
type: kata
---
## Goal
Wrap A8 bump arena as a pmr resource.
## Task
Implement resource that allocates from bump arena; test with pmr::vector.
## Acceptance
- [ ] All memory accounted in arena stats; reset clears containers.