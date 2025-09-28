---
title: B11 — Footguns & Sharp Edges (triage & patterns)
kit_id: b11_footguns
version: 1.0
status: Draft
category: C++ Core
assets: []
dependencies: []
---

## Objective
Spot and neutralize common C++ pitfalls: narrowing, dangling, ADL hijacks, lifetime confusion, order-of-evaluation, UB casts, ODR/linkage snares, and tricky conversions.

## Steps
1) Reproduce each pitfall in a tiny failing test, then apply a safe pattern.
2) Add compile-time guards (concepts/traits) and runtime checks where useful.
3) Document “why it failed” in 1–2 lines per kata for future code reviews.

## Smoke Test
- [ ] All “bad” variants fail first (or trigger sanitizers), then “good” variants pass.  
- [ ] Each kata leaves behind a short rule-of-thumb comment.

## Notes
Prefer explicitness: `explicit`, `enum class`, constrained templates, and lifetimes made visible (`span`/owners). Avoid cleverness that hides ownership or evaluation order.
