---
title: B9/k18 — Thread-safe lazy init (optional/cache)
kit_id: b9_concurrency
version: 1.0
status: Draft
type: kata
---
## Objective
Provide lazy construction of a cached value without races.
## Acceptance
- [ ] Exactly-one construction under heavy concurrency; no deadlocks; cache invalidation test included.
