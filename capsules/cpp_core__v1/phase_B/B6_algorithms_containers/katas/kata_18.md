---
title: B6/k18 — Timeout & cancellation contracts
kit_id: b6_errors_contracts
version: 1.0
status: Draft
type: kata
---
## Objective
Thread a `stop_token` and deadline through an operation and surface `timeout` as a first-class error.
## Acceptance
- [ ] Operation stops within bound and returns `timeout` error; cooperative cancellation path covered by test.
