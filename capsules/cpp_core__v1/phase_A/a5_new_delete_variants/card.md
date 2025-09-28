---
title: A5 — new/delete Variants
kit_id: a5_new_delete_variants
version: 1.0
status: Draft
category: Resource Management
assets: []
dependencies: [a0_on_ramp, a1_raii, a2_unique_ptr_deleters, a4_ownership_zoo]
---

## Objective
Understand and safely use C++ allocation forms: `new`, `new[]`, placement new, `delete`, `delete[]`, and why RAII wrappers beat raw usage.

## Setup
- Tooling: Catch2, ASan/UBSan.
- Compiler flags: `-Wall -Wextra -Wconversion -fsanitize=address`.

## Steps
1) Show difference between `new T` and `new T[n]`; match with `delete` vs `delete[]`.
2) Demonstrate **placement new** into a raw buffer; require explicit destructor call.
3) Highlight footguns: mismatched `new[]/delete`, forgetting destructor on placement, throwing constructors.
4) Prefer `std::make_unique` / `std::make_shared` for exceptions safety.
5) Show aligned allocation (`new(std::align_val_t{…})`) and cleanup in C++17+.

## Smoke Test
- [ ] Mismatched forms trigger ASan errors.  
- [ ] Placement new object constructed/destructed manually without leaks.

## Blueprint Hook (TL;DR for BP users)
**What transfers:** arrays must be freed consistently; explicit construction/destruction is rare in BP. Use pooled actors/components in one place, destroy in one place.  
**BP building blocks:** `AddComponent` (spawn), `DestroyComponent`; `SpawnActor`/`DestroyActor`; pooling systems.  
**Mini demo:** Pool actor manually adds/removes child components; Acceptance: no dangling components after destroy.

## Keep/Revert
KEEP: Aligned allocation callout.  
REVERT: Omit if target compiler lacks aligned new.