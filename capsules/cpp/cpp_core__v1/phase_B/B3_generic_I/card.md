---
title: B3 — Generic I (templates, overloads, ADL, SFINAE→concepts)
kit_id: b3_generic_I
version: 1.0
status: Draft
category: C++ Core
assets: []
dependencies: []
---


## Objective
Write expressive, safe, and efficient generic C++ using templates, overload sets, ADL, and modern **constraints** (from SFINAE to **concepts**).


## Steps
1) Function/class/alias/variable templates; deduction guides.
2) Overload sets, tag dispatch, and priority biasing.
3) ADL rules, customization points, and `using std::swap`.
4) SFINAE via detection idioms → `requires` clauses and named **concepts**.
5) `constexpr` and CTAD; compile-time computation and traits.


## Smoke Test
- [ ] All katas compile on Clang/GCC/MSVC; no ODR or ambiguity.
- [ ] Constraint errors are readable (friendly concepts).


## Notes
Prefer `requires`/concepts to SFINAE when possible; expose **customization points** via thin free functions in your namespace.