---
title: A2 — unique_ptr Deleters & Comparisons
kit_id: a2_unique_ptr_deleters
version: 1.0
status: Draft
category: Resource Management
assets: []
dependencies: [a0_on_ramp, a1_raii]
---

## Objective
Master `std::unique_ptr<T, D>` nuances: custom deleters (stateless/stateful), type/size trade‑offs, arrays (`T[]`), and safe comparisons (`get()`, `owner_before`, and pointee comparisons).

## Setup
- Tooling: Catch2, ASan/UBSan; enable warnings: `-Wall -Wextra -Wconversion`.

## Steps
1) Declare `using file_uptr = std::unique_ptr<FILE, int(*)(FILE*)>;` and with a functor deleter; observe type changes.
2) Demonstrate stateful deleter (stores a path or flag) and note `sizeof(unique_ptr)` growth; prefer EBO‑friendly deleters.
3) Use `std::unique_ptr<T[]>` with `std::default_delete<T[]>` for arrays; avoid mixing with `T` form.
4) Compare by **pointee** via helper (`less_by_value`) or deref, never raw address unless identity semantics are intended.
5) For associative containers, use `owner_before` to define strict weak ordering of owners.

## Smoke Test
- [ ] All sample tests compile and pass under sanitizers.  
- [ ] No mismatched `delete`/`delete[]` or double‑free.

## Blueprint Hook (TL;DR for BP users)
**What transfers:** explicit ownership & cleanup → set up in **BeginPlay**, release at **EndPlay**; use one place to allocate, one place to free.  
**BP building blocks:** `BeginPlay`/`EndPlay`, `SetLifeSpan`, `Unbind` delegates, `OnDestroyed`; arrays map to **component arrays** managed in one actor.  
**Mini demo:** Spawn an actor that registers to an event on BeginPlay and unbinds in EndPlay; Acceptance: no callbacks after destroy.

## Keep/Revert
KEEP: EBO + stateful deleter size callout.  
REVERT: Swap FILE* example for OS handle on platforms without C stdio.