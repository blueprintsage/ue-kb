---
title: A10/k3 — iterator invalidation cases
kit_id: a10_vector_forwardlist
version: 1.0
status: Draft
type: kata
---
## Goal
Catalog which operations invalidate iterators/pointers/references for vector and forward_list.
## Task
Run scenarios: push_back, insert at begin, erase middle, reserve, clear; assert validity expectations.
## Acceptance
- [ ] Tests fail when invalidated access occurs; documentation appended.