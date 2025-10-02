---
title: B8/k22 — Exceptions vs error codes in hot paths
kit_id: b8_perf_layout
version: 1.0
status: Draft
type: kata
---
## Objective
Measure cost of exception-disabled hot loops vs error-code returns.
## Acceptance
- [ ] Policy chosen with data; fast-path unaffected; failure-path cost charted.
