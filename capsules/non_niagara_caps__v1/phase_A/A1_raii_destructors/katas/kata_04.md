---
title: A1/k4 — exception safety (strong)
kit_id: a1_raii
version: 1.0
status: Draft
type: kata
---
## Goal
Prove no leaks if ctor throws; strong guarantee on operations.
## Task
Simulate throwing paths; verify invariants and no leaks.
## Acceptance
- [ ] Tests pass under ASan/UBSan with injected throws.