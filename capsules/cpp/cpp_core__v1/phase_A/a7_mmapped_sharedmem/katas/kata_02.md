---
title: A7/k2 — mmap RW + flush
kit_id: a7_mmapped_sharedmem
version: 1.0
status: Draft
type: kata
---
## Goal
Modify a mapped region and persist to disk.
## Task
Map RW; write a pattern; call `msync`/`FlushViewOfFile`.
## Acceptance
- [ ] File contents reflect changes after unmap.