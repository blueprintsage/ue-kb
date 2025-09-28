---
title: B6/k29 — Domain conversion at boundaries (service↔UI)
kit_id: b6_errors_contracts
version: 1.0
status: Draft
type: kata
---
## Objective
Map service-layer errors to user-facing messages without leaking internals.
## Acceptance
- [ ] Each service error maps to one of N UI strings; unmapped errors fall back to a safe generic message with trace code.
