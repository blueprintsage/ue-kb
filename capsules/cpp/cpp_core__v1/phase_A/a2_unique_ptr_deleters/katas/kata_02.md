---
title: A2/k2 — stateful deleter & size impact
kit_id: a2_unique_ptr_deleters
version: 1.0
status: Draft
type: kata
---
## Goal
Show how a stateful deleter increases `unique_ptr` size; prefer EBO when possible.
## Task
Make a deleter holding a small struct (e.g., `bool verbose`); `sizeof(unique_ptr<T, D>)` vs `sizeof(unique_ptr<T, default_delete<T>>)`.
## Acceptance
- [ ] Size difference observed; behavior identical; logs gated by state.