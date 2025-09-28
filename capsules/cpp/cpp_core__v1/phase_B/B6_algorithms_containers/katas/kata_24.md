---
title: B6/k24 — Postconditions with old-value capture
kit_id: b6_errors_contracts
version: 1.0
status: Draft
type: kata
---
## Objective
Check postconditions by capturing pre-state and verifying delta after mutation.
## Acceptance
- [ ] `ENSURES` validates invariant using saved `old`; failing variant reproduces readable message in debug.
