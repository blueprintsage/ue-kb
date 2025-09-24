---
title: A1 — RAII & Destructors (Ch4)
kit_id: a1_raii
version: 1.0
status: Draft
category: Resource Management
assets: []
dependencies: [a0_on_ramp]
---


## Objective
Master RAII: acquire/initialize in constructor, release in destructor; design move‑only types; ensure exception safety and correct destruction order.


## Setup
- Tooling: Catch2, clang‑tidy (modernize‑use‑using, performance‑*, readability‑*), ASan/UBSan.


## Steps
1) Implement a minimal RAII wrapper around a C resource (e.g., FILE*).
2) Add move constructor/assignment; delete copy.
3) Provide custom deleter injection; prove exception safety via tests.
4) Demonstrate base→derived destructor order and member destruction sequencing.


## Smoke Test
- [ ] Creating/closing path exercises pass under sanitizers.
- [ ] No leaks or double‑frees reported.


## Blueprint Hook (TL;DR for BP users)
**What transfers:** "init in one place, clean up automatically" → set up in BeginPlay / tear down in EndPlay or `OnDestroyed`.
**BP building blocks:** `BeginPlay`, `EndPlay`, `OnDestroyed`, `Bind Event to …` + `Unbind`, `SpawnActorDeferred` with `FinishSpawning`, `SetLifeSpan`.
**Mini demo:** Spawn a helper actor in BeginPlay, bind to a dispatcher, unbind in EndPlay; Acceptance: no binds remain after destroy.


## Keep/Revert
KEEP: Move‑only emphasis.
REVERT: Switch FILE* to OS handle if platform needs.