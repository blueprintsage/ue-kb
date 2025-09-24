---
title: A0 — On‑Ramp (Ch1)
kit_id: a0_on_ramp
version: 1.0
status: Draft
category: C++ Fundamentals
assets: []
dependencies: []
---


## Objective
Warm up core concepts used throughout Phase A: string & view lifetimes, stack vs heap object lifetime, and the "same‑bytes" intuition for representation.


## Setup
- Tooling: Catch2, clang‑tidy, clang‑format.
- Build: Debug + ASan enabled.


## Steps
1) Review `std::string` vs `std::string_view` lifetime and dangling hazards.
2) Contrast automatic (stack) and dynamic lifetimes; confirm destructor timing.
3) Examine representation with `std::bit_cast` to illustrate "same‑bytes" safely (no UB).


## Smoke Test
- [ ] All three sample tests compile and pass under ASan.


## Blueprint Hook (TL;DR for BP users)
**What transfers:** references vs owned objects → BP references & validity; lifetime awareness when creating widgets/actors.
**BP building blocks:** "Is Valid" checks, `Create Widget` on BeginPlay and `RemoveFromParent` on EndPlay, `SpawnActorDeferred` + `FinishSpawning`.
**Mini demo:** Create `WBP_Label`, add to viewport on BeginPlay, remove on EndPlay; Acceptance: no lingering widget after level change.


## Keep/Revert
KEEP: Hook wording ok.
REVERT: tighten examples after katas.