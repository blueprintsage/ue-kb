---
title: B10/k1 — Unique handle wrapper (custom deleter)
kit_id: b10_resources
version: 1.0
status: Draft
type: kata
---
## Objective
Wrap a C resource (e.g., FILE*/socket) in a `unique_handle` with callable deleter.
## Acceptance
- [ ] No leaks; deleter invoked exactly once; moves transfer ownership; copies disabled.
