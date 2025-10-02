---
title: B9/k15 — Thread pool sketch (fixed size)
kit_id: b9_concurrency
version: 1.0
status: Draft
type: kata
---
## Objective
Build a tiny fixed-size pool consuming a work queue.
## Acceptance
- [ ] Tasks execute exactly-once; pool joins cleanly; no data races under TSan.
