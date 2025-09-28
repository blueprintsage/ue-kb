---
title: B12/k6 — Perf guard (p95) on critical bench
kit_id: b12_capstone
version: 1.0
status: Draft
type: kata
---
## Objective
Protect a key benchmark with a p95 regression threshold.
## Acceptance
- [ ] CI fails if p95 exceeds baseline +10%; injected slowdown triggers guard; doc explains baseline updates.
