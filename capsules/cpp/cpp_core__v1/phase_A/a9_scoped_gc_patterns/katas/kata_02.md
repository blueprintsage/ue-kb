---
title: A9/k2 — scope_success / scope_fail
kit_id: a9_scoped_gc_patterns
version: 1.0
status: Draft
type: kata
---
## Goal
Differentiate success vs failure cleanup.
## Task
Implement `scope_success` & `scope_fail` variants; test which fires under throw/no-throw.
## Acceptance
- [ ] Exactly one of success/fail fires per run.