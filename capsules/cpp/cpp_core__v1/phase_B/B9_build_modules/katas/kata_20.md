---
title: B9/k20 — Priority inversion demo & mitigation
kit_id: b9_concurrency
version: 1.0
status: Draft
type: kata
---
## Objective
Simulate priority inversion on a mutex; mitigate via protocol (design note) or avoiding long holds.
## Acceptance
- [ ] Test shows starvation pre-mitigation; post-mitigation improves latency distribution.
