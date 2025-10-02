---
title: A10/k2 — relocation vs move/copy
kit_id: a10_vector_forwardlist
version: 1.0
status: Draft
type: kata
---
## Goal
Observe when vector relocates with `memmove` (trivially relocatable) vs move-construct/destroy.
## Task
Create type A (trivial) and type B (has throwing move). Push into vector, trigger reallocation, instrument constructor/move/dtor calls.
## Acceptance
- [ ] Trivial type uses memcpy; throwing move uses move+destroy paths.