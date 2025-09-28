---
title: A7/k5 — resize hazard
kit_id: a7_mmapped_sharedmem
version: 1.0
status: Draft
type: kata
---
## Goal
Demonstrate that shrinking the file invalidates the mapping; implement safe unmap+remap.
## Task
Truncate file after mapping; catch fault in test env; then rewrite with remap.
## Acceptance
- [ ] Safe path avoids crash; size checks gate access.