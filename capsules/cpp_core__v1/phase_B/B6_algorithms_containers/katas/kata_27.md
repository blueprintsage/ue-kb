---
title: B6/k27 — Partial construction guard (two-phase init)
kit_id: b6_errors_contracts
version: 1.0
status: Draft
type: kata
---
## Objective
Protect against exceptions during multi-step construction using builders/validators.
## Acceptance
- [ ] Object cannot leak half-initialized state; invalid intermediate states are unrepresentable or cleaned automatically.
