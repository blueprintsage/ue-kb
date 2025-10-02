---
title: B11/k8 — Lifetime of temporaries & ref-binding pitfalls
kit_id: b11_footguns
version: 1.0
status: Draft
type: kata
---
## Objective
Bind references to temporaries and show early destruction; fix with objects that own storage or value-return APIs.
## Acceptance
- [ ] Dangling usage detected; safe pattern passes and documents lifetime guarantee.
