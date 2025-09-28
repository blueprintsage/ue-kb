---
title: A13 — start_lifetime / relocation / type‑aware
kit_id: a13_start_lifetime
version: 1.0
status: Draft
category: Object Lifetimes
assets: []
dependencies: [a5_new_delete_variants, a8_allocators_arenas, a10_vector_forwardlist]
---


## Objective
Work safely with low‑level lifetime primitives and relocation semantics: **`std::start_lifetime_as`**, trivial relocation vs move/copy, and type‑aware aliasing. Learn when byte copies are valid and how to avoid UB while optimizing.


## Setup
- Tooling: Catch2; compile with `-std=c++23` for `start_lifetime_as`.


## Steps
1) **start_lifetime_as**: re‑initialize storage as an object of type T and use it legally.
2) **Trivial relocation**: detect trivially relocatable types (proxy via `is_trivially_move_constructible && is_trivially_destructible`) and use `memcpy` for bulk move.
3) **Type‑aware views**: use `std::bit_cast` and spans of bytes vs typed spans with alignment checks.


## Smoke Test
- [ ] start_lifetime paths compile/run without UB under sanitizer.
- [ ] memcpy relocation used only for trivially relocatable proxy conditions.


## Blueprint Hook (TL;DR for BP users)
**What transfers:** treat raw memory tricks as **engine‑level** concerns; in BP, prefer safe high‑level APIs.
**BP building blocks:** avoid casting; use proper types and data tables; if raw buffers required (plugins), isolate in C++.


## Keep/Revert
KEEP: trivially relocatable proxy; REVERT: omit if toolchain lacks C++23 feature.