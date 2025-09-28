---
title: B6/k16 — Scope guards (defer / finally / unique_exit)
kit_id: b6_errors_contracts
version: 1.0
status: Draft
type: kata
---
## Objective
Provide RAII scope guards for success/failure/always-exit paths.
## Acceptance
- [ ] `on_success` fires only when no exception escapes; `on_failure` fires on exception; `defer` always fires; all are noexcept.
