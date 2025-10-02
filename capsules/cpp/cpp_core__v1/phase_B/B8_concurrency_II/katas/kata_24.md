---
title: B8/k24 — Link-time options: LTO, ICF, sectioning
kit_id: b8_perf_layout
version: 1.0
status: Draft
type: kata
---
## Objective
Test LTO/ThinLTO, identical code folding, -ffunction-sections/-Wl,--gc-sections.
## Acceptance
- [ ] Size drop and/or speed gain recorded; fallback path documented for MSVC.
