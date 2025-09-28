---
title: B12/k1 — Public API surface compiles standalone
kit_id: b12_capstone
version: 1.0
status: Draft
type: kata
---
## Objective
Ensure each public header compiles alone (include what you use).
## Acceptance
- [ ] `api_surface.tests.cpp` includes each header in isolation and builds clean on GCC/Clang/MSVC.
