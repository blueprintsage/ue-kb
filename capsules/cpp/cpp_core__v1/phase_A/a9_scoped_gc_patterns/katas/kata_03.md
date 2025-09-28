---
title: A9/k3 — unique_resource
kit_id: a9_scoped_gc_patterns
version: 1.0
status: Draft
type: kata
---
## Goal
RAII a (handle, deleter) pair with reset/release.
## Task
Wrap a FILE*/fd; test reset(), release(), swap().
## Acceptance
- [ ] Deleter runs exactly once; release prevents double-close.