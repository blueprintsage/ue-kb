---
title: B1/k1 — Value Categories & Overload Resolution
kit_id: b1_fundamentals_I
version: 1.0
status: Draft
type: kata
---
## Objective
Demonstrate how lvalues/xvalues/prvalues select overloads.
## Tasks
- Create `f(T&)`, `f(T const&)`, `f(T&&)`; call with lvalue, `std::move`, and a prvalue; assert chosen overload.
## Acceptance
- [ ] Overload logs match expected value category.
- [ ] No dangling refs; prvalue lifetime not extended accidentally.