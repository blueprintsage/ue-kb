---
title: B1 — Fundamentals I (types, refs, RAII, move/forward)
kit_id: b1_fundamentals_I
version: 1.0
status: Draft
category: C++ Core
assets: []
dependencies: []
---


## Objective
Establish rock‑solid basics: value categories, references/ownership, object lifetime, RAII, copy/move semantics, and perfect forwarding.


## Steps
1) **Value categories:** lvalue/xvalue/prvalue; decay/temporary lifetimes.
2) **References & const:** lvalue/rvalue refs, cv‑qualification, ref collapsing.
3) **RAII:** ctor/dtor invariants; Rule of Zero/Five; no raw new/delete in user code.
4) **Copy/move:** default/delete; noexcept moves; copy elision.
5) **Forwarding:** `std::forward` correctness; universal/forwarding refs.
6) **Init:** brace vs paren; aggregate vs custom; `= default`/`= delete`.


## Smoke Test
- [ ] All katas compile with sanitizers on; no UB; static analyzers clean.
- [ ] Unit tests show correct ownership/moves and no double‑free/leaks.


## Notes
Prefer **value semantics** by default; introduce indirection (smart ptr) only for shared or polymorphic ownership.