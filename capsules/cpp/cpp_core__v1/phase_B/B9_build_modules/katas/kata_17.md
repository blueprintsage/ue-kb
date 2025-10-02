---
title: B9/k17 — Atomic flags & fence correctness
kit_id: b9_concurrency
version: 1.0
status: Draft
type: kata
---
## Objective
Publish-read pattern using release/acquire with explicit fences.
## Acceptance
- [ ] Reordering bug reproduced without fences; fixed with release/acquire; verified by litmus/TSan.
