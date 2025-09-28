---
title: B8/k13 — False sharing probe (cache lines)
kit_id: b8_perf_layout
version: 1.0
status: Draft
type: kata
---
## Objective
Show slowdown from adjacent-thread writes and fix with padding/alignas.
## Acceptance
- [ ] Padded version eliminates slowdown; TSan clean (if enabled).
