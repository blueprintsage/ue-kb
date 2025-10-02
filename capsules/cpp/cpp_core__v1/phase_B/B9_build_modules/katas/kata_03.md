---
title: B9/k3 — Deadlock reproduction and fix
kit_id: b9_concurrency
version: 1.0
status: Draft
type: kata
---
## Objective
Reproduce a two-lock deadlock, then fix with `std::scoped_lock` or lock ordering.
## Acceptance
- [ ] Failing test hangs (with timeout) pre-fix; post-fix completes reliably.
