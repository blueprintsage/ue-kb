---
title: B6/k5 — noexcept correctness matrix
kit_id: b6_errors_contracts
version: 1.0
status: Draft
type: kata
---
## Objective
Model `noexcept` on move/ctor/swap and prove propagation into containers.
## Acceptance
- [ ] Table-driven tests confirm container operations choose fast paths when noexcept is true.
