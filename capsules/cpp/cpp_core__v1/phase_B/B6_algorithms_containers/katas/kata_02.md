---
title: B6/k2 — expected<T,E> pipeline
kit_id: b6_errors_contracts
version: 1.0
status: Draft
type: kata
---
## Objective
Compose `expected` with `and_then`/`or_else` and show single-pass error propagation.
## Acceptance
- [ ] Success path runs all stages; first failure skips downstream and returns correct `E`.
