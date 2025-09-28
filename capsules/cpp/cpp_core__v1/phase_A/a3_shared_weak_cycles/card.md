---
title: A3 — shared_ptr / weak_ptr & Cycles (Ch5)
kit_id: a3_shared_weak_cycles
version: 1.0
status: Draft
category: Resource Management
assets: []
dependencies: [a0_on_ramp, a1_raii]
---

## Objective
Use `std::shared_ptr` safely (control block, aliasing ctor, thread-safety notes) and break ownership cycles with `std::weak_ptr`. Learn when **shared** is warranted vs **unique**, and how to observe without owning.

## Setup
- Tooling: Catch2, ASan/UBSan; `-Wall -Wextra -Wconversion`.

## Steps
1) Create two objects that reference each other; show leak when both use `shared_ptr` (cycle).
2) Replace one side with `weak_ptr` to break the cycle; use `.lock()` carefully.
3) Demonstrate **aliasing constructor** to share the control block while pointing at a subobject (lifetime ties).
4) Inspect refcounts with `use_count()` only in tests; avoid in logic. Note atomic increments on copies.
5) Prefer `make_shared<T>` for fewer allocations; call out `enable_shared_from_this` and its pitfalls.

## Smoke Test
- [ ] Cycle case leaks under ASan; weak fix removes leak.  
- [ ] Aliasing ctor keeps subobject alive as long as owner shared exists.

## Blueprint Hook (TL;DR for BP users)
**What transfers:** avoid hidden cycles (Actor ↔ Component, widget ↔ owner). Keep one owner; others hold non-owning refs.  
**BP building blocks:** use **weak references** (Soft Object References, weak pointers in C++-backed BPs), and clear bindings in `EndPlay`.  
**Mini demo:** Actor A binds to B's dispatcher; A unbinds in `EndPlay` and clears `Target` ref; Acceptance: no callbacks after destroy, no garbage refs in log.

## Keep/Revert
KEEP: Aliasing constructor + `enable_shared_from_this` callouts.  
REVERT: Add `atomic_shared_ptr` note if we adopt C++20 P0718 impl later.