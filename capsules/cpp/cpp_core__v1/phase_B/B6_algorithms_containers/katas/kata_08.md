---
title: B6/k8 — Exception ↔ error_code boundary
kit_id: b6_errors_contracts
version: 1.0
status: Draft
type: kata
---
## Objective
Convert exceptions to `error_code` at module boundaries and back where needed.
## Acceptance
- [ ] Boundary adapter round-trips representative failures without losing information.
