---
title: A7/k6 — MAP_PRIVATE / CoW
kit_id: a7_mmapped_sharedmem
version: 1.0
status: Draft
type: kata
---
## Goal
Write to a private mapping and show disk unchanged.
## Task
POSIX only: `MAP_PRIVATE` mapping; write; compare file before/after.
## Acceptance
- [ ] On‑disk bytes unchanged; mapping shows edits.