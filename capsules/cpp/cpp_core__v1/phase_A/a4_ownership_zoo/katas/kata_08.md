---
title: A4/k8 — API design: observer in, owner out
kit_id: a4_ownership_zoo
version: 1.0
status: Draft
type: kata
---
## Goal
Design a small API where creation returns an owner, but processing functions accept observers.
## Task
`auto r = make_resource(); process(*r);` Verify signatures communicate ownership clearly.
## Acceptance
- [ ] Call sites read clearly; tests pass.