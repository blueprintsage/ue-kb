---
title: B9/k10 — Thread-safe queue (minimal work queue)
kit_id: b9_concurrency
version: 1.0
status: Draft
type: kata
---
## Objective
Provide `push`, `try_pop`, and `close` semantics with shutdown signaling.
## Acceptance
- [ ] No races; consumers exit when closed; stress test passes under TSan.
