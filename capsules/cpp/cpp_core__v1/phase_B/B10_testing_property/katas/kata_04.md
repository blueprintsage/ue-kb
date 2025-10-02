---
title: B10/k4 — Type erasure with small-buffer optimization
kit_id: b10_resources
version: 1.0
status: Draft
type: kata
---
## Objective
Implement a `function_ref`/`any_invocable`-style object with SBO threshold.
## Acceptance
- [ ] Small callables stored inline; big ones heap-allocate; call correctness proven; no leaks.
