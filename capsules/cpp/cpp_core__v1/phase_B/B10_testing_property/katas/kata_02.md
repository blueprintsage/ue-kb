---
title: B10/k2 — Shared/weak ownership & cycle break
kit_id: b10_resources
version: 1.0
status: Draft
type: kata
---
## Objective
Demonstrate a cycle with `shared_ptr` and fix using `weak_ptr`.
## Acceptance
- [ ] Leak reproduced pre-fix; post-fix frees both nodes; refcounts observed in tests.
