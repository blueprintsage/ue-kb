---
title: B8/k10 — Format/parse costs (std::format vs iostreams)
kit_id: b8_perf_layout
version: 1.0
status: Draft
type: kata
---
## Objective
Compare `std::format`, `fmt`, and iostreams in hot loops.
## Acceptance
- [ ] Faster option chosen with p95 data; allocations counted; locale effects noted.
