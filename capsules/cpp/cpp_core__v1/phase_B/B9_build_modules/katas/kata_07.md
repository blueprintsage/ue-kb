---
title: B9/k7 — False sharing probe and padding fix
kit_id: b9_concurrency
version: 1.0
status: Draft
type: kata
---
## Objective
Demonstrate cache-line contention and remediate with `alignas(64)` or struct padding.
## Acceptance
- [ ] Padded version is ≥2× faster on tight loops with adjacent thread writes.
