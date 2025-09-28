---
title: B6/k7 — Parser fuzz tripwire (contracts)
kit_id: b6_errors_contracts
version: 1.0
status: Draft
type: kata
---
## Objective
Fuzz a tiny parser; on invariant violation, emit seed + minimal shrink.
## Acceptance
- [ ] 1K random inputs run; any failure reports reproducible seed and shrunk case.
