---
title: B6/k3 — error_code domain & category
kit_id: b6_errors_contracts
version: 1.0
status: Draft
type: kata
---
## Objective
Define a custom `error_category` with stable names/messages and equality semantics.
## Acceptance
- [ ] `make_error_code(x)` compares equal across copies and prints friendly text.
