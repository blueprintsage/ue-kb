---
title: B10/k3 — pImpl (handle/body) with stable ABI
kit_id: b10_resources
version: 1.0
status: Draft
type: kata
---
## Objective
Hide implementation in `.cpp` via pImpl; maintain stable header/API.
## Acceptance
- [ ] Header compiles standalone; copy/move semantics correct; ODR safe; size of public type is a pointer.
