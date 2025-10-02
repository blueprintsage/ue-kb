---
title: B6/k6 — Destructor-safe guard
kit_id: b6_errors_contracts
version: 1.0
status: Draft
type: kata
---
## Objective
Design a RAII wrapper that never throws in destructors and records cleanup result.
## Acceptance
- [ ] All destructor paths are `noexcept(true)`; cleanup observable via probe.
