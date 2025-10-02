---
title: B1/k2 — Reference Collapsing & Forwarding Refs
kit_id: b1_fundamentals_I
version: 1.0
status: Draft
type: kata
---
## Objective
Show `T& & → T&`, `T& && → T&`, `T&& & → T&`, `T&& && → T&&` in templates.
## Tasks
- Implement `wrapper<T>::call(U&& u)`; static_assert the deduced `U` and collapsed type using helper traits.
## Acceptance
- [ ] All four collapse cases verified by unit tests.