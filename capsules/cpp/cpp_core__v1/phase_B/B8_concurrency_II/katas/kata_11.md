---
title: B8/k11 — String building: reserve, append, join
kit_id: b8_perf_layout
version: 1.0
status: Draft
type: kata
---
## Objective
Reduce reallocs while building large strings.
## Acceptance
- [ ] `reserve`/join approach dominates naive `operator+`; alloc chart included.
