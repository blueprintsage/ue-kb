---
title: B6/k15 — Retry with backoff & idempotency contract
kit_id: b6_errors_contracts
version: 1.0
status: Draft
type: kata
---
## Objective
Implement a retry wrapper that only repeats idempotent operations.
## Acceptance
- [ ] Non-idempotent op is refused (contract violation in debug); idempotent op retries with capped backoff and succeeds in test rig.
