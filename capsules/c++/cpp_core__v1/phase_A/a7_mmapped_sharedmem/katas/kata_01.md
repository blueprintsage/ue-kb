---
title: A7/k1 — mmap RO sum
kit_id: a7_mmapped_sharedmem
version: 1.0
status: Draft
type: kata
---
## Goal
Map a binary file of uint32_t and sum values without copying.
## Task
Open → mmap RO → `span<uint32_t const>` → accumulate.
## Acceptance
- [ ] Sum matches reference buffered read.