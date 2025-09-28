---
title: A9/k1 — scope_exit (always)
kit_id: a9_scoped_gc_patterns
version: 1.0
status: Draft
type: kata
---
## Goal
Run cleanup code on scope exit for both success and failure paths.
## Task
Implement `scope_exit` (or use GSL `final_action`); verify it fires on return and throw.
## Acceptance
- [ ] Guard triggers exactly once in both cases.