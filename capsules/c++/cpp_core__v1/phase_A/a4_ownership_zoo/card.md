---
title: A4 — Ownership Zoo: non‑owning, non‑null, duplicate handles
kit_id: a4_ownership_zoo
version: 1.0
status: Draft
category: Resource Management
assets: []
dependencies: [a0_on_ramp, a1_raii, a2_unique_ptr_deleters]
---

## Objective
Use the right pointer/handle flavor for the job: **owning** (`unique_ptr`), **observing** (raw pointer/reference or gsl::not_null<T*>), **non‑null contracts**, and **duplicate handles** (OS/file descriptors) with correct close semantics.

## Setup
- Tooling: Catch2, ASan/UBSan; enable `-Wall -Wextra -Wconversion`.
- Optional: GSL (Guidelines Support Library) or gsl‑lite for `not_null`.

## Steps
1) **Observing vs Owning:** Pass **references** for required observers, **T* (nullable)** for optional observers; document ownership in type.
2) **Non‑null contract:** Wrap non‑nullable observers in `gsl::not_null<T*>` (or assert in ctor) to encode invariants.
3) **Unique owners:** Keep a single `std::unique_ptr<T>` as the owner; provide `T&`/`T*` views to callers.
4) **Duplicate handles:** Model OS handle duplication with a tiny RAII wrapper that calls the matching close exactly once per live handle copy; prohibit copy or implement ref‑counted dup.
5) **Lifetimes in containers:** Store owners by value (inside container of `unique_ptr<T>`), expose observers when iterating; no raw owning pointers.
6) **APIs:** Factories return owners; setters take owners by value (move) or observers by reference/pointer based on intent.

## Smoke Test
- [ ] No double‑close/dangling observer under sanitizers.  
- [ ] Non‑null invariants enforced at boundaries.

## Blueprint Hook (TL;DR for BP users)
**What transfers:** keep *one* owner, pass around **references** elsewhere; clear observers on destroy.  
**BP building blocks:** Components own subobjects; other actors hold **soft refs**/Object refs; clear in `EndPlay` and unbind delegates.  
**Mini demo:** Manager actor owns a pooled component array; outside actors store an **object reference variable** (nullable). Acceptance: when manager is destroyed, outside actors detect null and skip use.

## Keep/Revert
KEEP: Duplicate‑handle RAII wrapper pattern.  
REVERT: If GSL isn’t available, keep a minimal `not_null` shim inside tests only.