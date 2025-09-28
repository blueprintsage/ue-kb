---
title: A2/k3 — arrays via unique_ptr<T[]>
kit_id: a2_unique_ptr_deleters
version: 1.0
status: Draft
type: kata
---
## Goal
Manage dynamic arrays with `unique_ptr<T[]>` and verify `delete[]` is used.
## Task
Allocate `unique_ptr<int[]>` length N, fill & sum; confirm deallocation under ASan with no leaks.
## Acceptance
- [ ] Sum correct; sanitizer shows no mismatched delete.