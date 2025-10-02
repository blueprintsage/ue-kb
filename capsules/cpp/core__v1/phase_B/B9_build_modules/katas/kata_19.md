---
title: B9/k19 — Cancellation plumbed through pipelines
kit_id: b9_concurrency
version: 1.0
status: Draft
type: kata
---
## Objective
Thread `stop_token` through a multi-stage pipeline and handle early exit.
## Acceptance
- [ ] Mid-pipeline cancel stops all stages promptly; resources released deterministically.
