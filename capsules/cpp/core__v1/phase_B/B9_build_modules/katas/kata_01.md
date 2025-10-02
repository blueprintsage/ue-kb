---
title: B9/k1 — jthread with cooperative stop
kit_id: b9_concurrency
version: 1.0
status: Draft
type: kata
---
## Objective
Start a `std::jthread` and honor `stop_token` promptly.
## Acceptance
- [ ] Worker exits within ≤10ms of `request_stop()` in test harness; no leaks.

