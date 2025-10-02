---
title: B2/k14 — Memory‑mapped File Read
kit_id: b2_fundamentals_II
version: 1.0
status: Draft
type: kata
---
## Objective
Read a large file with mmap (or Win32 MapView) and iterate via `span`.
## Acceptance
- [ ] Faster than buffered I/O for large files; unmaps safely.