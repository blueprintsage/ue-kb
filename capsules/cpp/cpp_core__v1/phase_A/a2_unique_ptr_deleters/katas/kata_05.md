---
title: A2/k5 — owner_before ordering for assoc containers
kit_id: a2_unique_ptr_deleters
version: 1.0
status: Draft
type: kata
---
## Goal
Demonstrate `owner_before` for ordering owners without dereferencing.
## Task
Insert several `unique_ptr<int>` into `std::set` using a custom key comparator that calls `owner_before`.
## Acceptance
- [ ] Set contains one element per owner; no UB; iteration stable.