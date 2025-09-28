---
title: A13/k1 — start_lifetime_as
kit_id: a13_start_lifetime
version: 1.0
status: Draft
type: kata
---
## Goal
Reinitialize storage for another T safely using `std::start_lifetime_as<T>`.
## Task
Create raw storage (aligned_storage or array of bytes), construct T, then start lifetime as U and use; verify invariants.
## Acceptance
- [ ] No UB; sanitizers clean.