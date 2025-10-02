---
title: B6/k17 — Transactional commit/rollback RAII
kit_id: b6_errors_contracts
version: 1.0
status: Draft
type: kata
---
## Objective
Model a transaction object that stages changes and commits or rolls back on scope exit.
## Acceptance
- [ ] Throwing mid-transaction leaves external state unchanged; explicit `commit()` persists changes; coverage shows both branches.
