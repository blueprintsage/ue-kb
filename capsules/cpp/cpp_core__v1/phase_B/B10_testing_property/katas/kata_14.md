---
title: B10/k14 — Observer vs owner pointers (non-owning)
kit_id: b10_resources
version: 1.0
status: Draft
type: kata
---
## Objective
Use `observer_ptr<T>`-like semantics to make non-ownership explicit.
## Acceptance
- [ ] Static analysis/tests show no deref after owner destruction; docs call out lifetime contracts.
