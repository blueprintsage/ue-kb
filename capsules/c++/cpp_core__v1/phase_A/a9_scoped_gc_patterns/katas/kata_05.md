---
title: A9/k5 — exception safety
kit_id: a9_scoped_gc_patterns
version: 1.0
status: Draft
type: kata
---
## Goal
Throw mid-function and ensure guards clear partial state.
## Task
Allocate two resources; throw after first; verify guard cleaned it.
## Acceptance
- [ ] Sanitizers show zero leaks on throw path.