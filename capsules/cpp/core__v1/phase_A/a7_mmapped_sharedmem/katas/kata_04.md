---
title: A7/k4 — RAII map wrapper
kit_id: a7_mmapped_sharedmem
version: 1.0
status: Draft
type: kata
---
## Goal
Encapsulate map/unmap with proper dtor.
## Task
`class mapping{void* p; size_t n; ~mapping(){unmap();}};` expose `span<std::byte>`.
## Acceptance
- [ ] Unmap called exactly once; tests pass under sanitizer.