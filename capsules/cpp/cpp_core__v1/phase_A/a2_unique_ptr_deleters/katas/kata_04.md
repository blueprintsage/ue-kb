---
title: A2/k4 — compare by pointee value
kit_id: a2_unique_ptr_deleters
version: 1.0
status: Draft
type: kata
---
## Goal
Sort a vector of `unique_ptr<int>` by the **values** they point to, not addresses.
## Task
Provide comparator `cmp = [](auto const& a, auto const& b){ return *a < *b; };` and prove strict weak ordering.
## Acceptance
- [ ] Sorted order matches values; tests cover duplicates/ties.