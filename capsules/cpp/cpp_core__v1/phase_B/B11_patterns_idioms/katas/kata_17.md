---
title: B11/k17 — Volatile is not a synchronization primitive
kit_id: b11_footguns
version: 1.0
status: Draft
type: kata
---
## Objective
Show that `volatile` doesn’t make operations atomic or ordered; fix with atomics/mutexes.
## Acceptance
- [ ] Racy volatile test fails; atomic/mutex solution passes and TSan is clean.
