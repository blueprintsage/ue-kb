---
title: A6 — Leak Detectors
kit_id: a6_leak_detectors
version: 1.0
status: Draft
category: Diagnostics
assets: []
dependencies: [a1_raii, a2_unique_ptr_deleters, a3_shared_weak_cycles]
---

## Objective
Detect and localize memory leaks: sanitizers (ASan/LSan), CRT leak reports (Windows), valgrind (Linux), and custom lightweight guards for CI.

## Setup
- Build with `-fsanitize=address,leak` (Clang/GCC) when available.
- Windows: `_CrtSetDbgFlag(_CRTDBG_ALLOC_MEM_DF | _CRTDBG_LEAK_CHECK_DF);`

## Steps
1) **Sanitizers first:** enable ASan/LSan; demonstrate a deliberate leak and read the report.
2) **CRT/Valgrind:** use platform tool to cross‑check leak location.
3) **Custom guard:** implement `leak_guard` that snapshots allocations on scope enter/exit (debug builds only) to flag growth.

## Smoke Test
- [ ] Deliberate leak detected by at least one tool.  
- [ ] Custom guard flags growth and reports counts.

## Blueprint Hook (TL;DR for BP users)
**What transfers:** measure, don’t guess. Track spawned actors/components and verify cleanup on level transition.  
**BP building blocks:** `Get All Actors Of Class` or actor tagging; compare counts before/after play session.  
**Mini demo:** Spawn N actors via BP, end the round, ensure counts return to baseline; Acceptance: delta = 0.

## Keep/Revert
KEEP: Cross‑platform tool matrix.  
REVERT: Skip `leak_guard` if tooling isn’t allowed in target.