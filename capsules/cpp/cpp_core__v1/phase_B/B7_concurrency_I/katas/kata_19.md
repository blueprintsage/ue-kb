---
title: B7/k19 — Reproducer pack (one command)
kit_id: b7_build_tooling
version: 1.0
status: Draft
type: kata
---
## Objective
Bundle failing test + compile_commands + last logs into a single zip.
## Acceptance
- [ ] `pack.sh` produces archive under `out/repro/`; handoff reproduces failure on a clean machine.
