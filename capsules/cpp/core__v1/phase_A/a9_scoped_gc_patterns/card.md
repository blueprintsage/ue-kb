---
title: A9 — Scoped GC Patterns
kit_id: a9_scoped_gc_patterns
version: 1.0
status: Draft
category: Resource Management
assets: []
dependencies: [a1_raii, a2_unique_ptr_deleters, a4_ownership_zoo, a5_new_delete_variants]
---

## Objective
Emulate “garbage collection” discipline with **scope-bound cleanup** and **deterministic lifetimes**: scope guards, `unique_resource`/`scope_exit`, ownership handoff, and bulk teardown.

## Setup
- Tooling: Catch2; enable ASan/UBSan for leak/UB checks.

## Steps
1) **Scope guard**: execute a lambda on scope exit (success/failure/both) to close/undo.
2) **`std::unique_ptr` as GC root**: own trees/graphs at the top; children hold observers.
3) **`std::unique_resource` (P0052-style)**: tie a resource + deleter; show swapping/reset.
4) **Bulk teardown**: group owners in a container, release on scope end (arena/pool synergy).
5) **Error paths**: prove no leaks on exceptions—guards fire; use `noexcept` destructors.

## Smoke Test
- [ ] Guards trigger on all early returns/throws.  
- [ ] No leaks; destructors run exactly once.

## Blueprint Hook (TL;DR for BP users)
**What transfers:** bind once, unbind at EndPlay; group spawns by **session** and destroy in one step.  
**BP building blocks:** `OnDestroyed`, `Unbind`, arrays of spawned actors/components with a single cleanup loop.  
**Mini demo:** Spawn 20 helpers on BeginPlay; on EndPlay, loop and Destroy; Acceptance: leaving the map leaves zero helpers.

## Keep/Revert
KEEP: success/failure/both variants of scope guard.  
REVERT: If `unique_resource` isn’t available, provide a minimal shim.