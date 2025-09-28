---
title: B8/k6 — pmr::polymorphic_allocator pool vs default
kit_id: b8_perf_layout
version: 1.0
status: Draft
type: kata
---
## Objective
Use a monotonic/pool resource for small allocations.
## Acceptance
- [ ] Alloc count reduced ≥50% vs default; p95 improves or holds; leak-free.
