---
title: B6/k26 — Exception-safe copy-on-write (COW) wrapper
kit_id: b6_errors_contracts
version: 1.0
status: Draft
type: kata
---
## Objective
Implement a small COW type that preserves invariants across throwing clones.
## Acceptance
- [ ] Throw during detach leaves source unchanged; moves/copies obey noexcept where applicable.
