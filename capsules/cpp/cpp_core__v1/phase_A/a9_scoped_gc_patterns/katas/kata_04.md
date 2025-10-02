---
title: A9/k4 — bulk teardown
kit_id: a9_scoped_gc_patterns
version: 1.0
status: Draft
type: kata
---
## Goal
Destroy a group of owners in one shot at scope end.
## Task
Keep `vector<unique_ptr<T>>` in a function scope; on exit, all Ts destruct; assert counts.
## Acceptance
- [ ] Destructors count equals pushed objects; no leaks.