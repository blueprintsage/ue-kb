---
title: B1/k19 — Perfect Forwarding Pitfalls
kit_id: b1_fundamentals_I
version: 1.0
status: Draft
type: kata
---
## Objective
Avoid forwarding into overload sets that change meaning.
## Tasks
- Build a factory that forwards to ctors; add static_asserts/examples where forwarding leads to narrowing or ambiguity; fix with tag dispatch.
## Acceptance
- [ ] No surprising picks; unit tests lock intended overloads.