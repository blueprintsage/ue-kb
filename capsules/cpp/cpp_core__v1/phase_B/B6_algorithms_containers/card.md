---
title: B6 — Errors & Contracts (robustness)
kit_id: b6_errors_contracts
version: 1.0
status: Draft
category: C++ Core
assets: []
dependencies: []
---

## Objective
Choose and justify error strategies (exceptions, status codes, or `expected`-style) and encode **contracts** to prevent invalid states.

## Steps
1) Exception safety levels (basic/strong/nothrow); throwing vs `noexcept`.
2) `std::error_code` / custom categories; mapping from failures to domains.
3) `std::expected`-style flows; composition with `and_then` / `or_else`.
4) Contracts: pre/post/invariants via asserts, concept checks, and guards.
5) Boundaries: destructor safety, panic/fail-fast policy, and logging taxonomy.

## Smoke Test
- [ ] Each kata compiles with sanitizers; failure paths exercised in tests.  
- [ ] Contract violations are caught in debug; release behavior documented.

## Notes
Prefer **representable invariants** over runtime checks; pick one error style per boundary and convert at edges (not everywhere).
