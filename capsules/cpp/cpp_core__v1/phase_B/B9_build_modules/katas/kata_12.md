---
title: B9/k12 — ABA hazard demo (atomics)
kit_id: b9_concurrency
version: 1.0
status: Draft
type: kata
---
## Objective
Reproduce ABA on a naive lock-free stack; fix with tagged pointers or counters.
## Acceptance
- [ ] Test catches ABA corruption pre-fix; post-fix passes under stress.
