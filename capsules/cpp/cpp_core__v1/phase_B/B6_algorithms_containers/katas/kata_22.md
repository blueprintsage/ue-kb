---
title: B6/k22 — expected<T,E> at module boundary (no exceptions across)
kit_id: b6_errors_contracts
version: 1.0
status: Draft
type: kata
---
## Objective
Return `expected` from a boundary and convert to exceptions only at the UI layer.
## Acceptance
- [ ] Service boundary exposes only `expected`; UI adapter throws on error; both paths tested.
