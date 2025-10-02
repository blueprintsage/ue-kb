---
title: B10/k13 — Intrusive refcounted handle (add_ref/release)
kit_id: b10_resources
version: 1.0
status: Draft
type: kata
---
## Objective
Build a minimal intrusive RC type with thread-safe counters.
## Acceptance
- [ ] No leaks/double-frees; counts hit zero exactly once; move/copy semantics documented and tested.
