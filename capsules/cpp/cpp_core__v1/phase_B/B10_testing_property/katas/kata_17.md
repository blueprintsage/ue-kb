---
title: B10/k17 — Resource pools (object reuse)
kit_id: b10_resources
version: 1.0
status: Draft
type: kata
---
## Objective
Create a small pool that hands out reusable objects with return-to-pool semantics.
## Acceptance
- [ ] No leaks; max in-use tracked; contention-free single-thread, safe multi-thread variant optional.
