---
title: A7/k3 — anonymous shared
kit_id: a7_mmapped_sharedmem
version: 1.0
status: Draft
type: kata
---
## Goal
Create a shared memory region visible in two mappings.
## Task
POSIX: `shm_open`+`ftruncate`+`mmap` twice; Win: two MapViewOfFile handles.
## Acceptance
- [ ] Writes in one view appear in the other.