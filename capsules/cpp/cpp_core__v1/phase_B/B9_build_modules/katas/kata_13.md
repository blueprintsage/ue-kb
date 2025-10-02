---
title: B9/k13 — Backoff & fairness (spin vs yield vs sleep)
kit_id: b9_concurrency
version: 1.0
status: Draft
type: kata
---
## Objective
Compare contention management strategies on a spinlock prototype.
## Acceptance
- [ ] Backoff reduces CPU burn without hurting throughput; fairness metrics logged.
