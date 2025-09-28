---
title: A11 — Implicit Mgmt Variants
kit_id: a11_implicit_mgmt_variants
version: 1.0
status: Draft
category: Resource Management
assets: []
dependencies: [a2_unique_ptr_deleters, a3_shared_weak_cycles]
---


## Objective
Explore smart pointer extensions and wrappers that **hide ownership details**: `observer_ptr`, `gsl::not_null`, `std::optional<T&>`, and other implicit helpers. Clarify safe vs unsafe implicit ownership and when to avoid over-abstraction.


## Setup
- Tooling: Catch2; GSL headers for `not_null` and `observer_ptr`.


## Steps
1) **observer_ptr**: non-owning raw pointer wrapper; check comparisons, nullability, conversions.
2) **not_null**: guarantee non-null invariant; test construction from raw, move, and runtime checks.
3) **Optional ref**: simulate nullable reference via `optional<reference_wrapper<T>>`; prove assignment and reset semantics.
4) **Implicit conversions**: measure safety tradeoffs; show compile errors where conversions prevent UB.


## Smoke Test
- [ ] `observer_ptr` acts like raw but disallows ownership; nullptr valid.
- [ ] `not_null` rejects nullptr at compile or runtime.
- [ ] Optional-ref correctly resets and rebinds.


## Blueprint Hook (TL;DR for BP users)
**What transfers:** explicit vs implicit links in Blueprints; always mark required refs vs optional.
**BP building blocks:** BP `Reference` vs `Soft Reference`; validate not-null in BeginPlay; optional refs handled with `IsValid` checks.
**Mini demo:** Character has optional Hat ref; if valid, apply material; Acceptance: no crash when Hat missing.


## Keep/Revert
KEEP: `not_null` + optional-ref; REVERT: skip `observer_ptr` if GSL not available.