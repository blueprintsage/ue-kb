---
title: B1/k20 — Move‑only Types in Containers
kit_id: b1_fundamentals_I
version: 1.0
status: Draft
type: kata
---
## Objective
Use `std::unique_ptr`/move‑only handles inside vectors/maps.
## Tasks
- Emplace and move; avoid copies; test reallocation behavior.
## Acceptance
- [ ] Compiles without copy ops; no leaks; iterators valid after moves.