---
title: B12 — Capstone (integrate & ship)
kit_id: b12_capstone
version: 1.0
status: Draft
category: C++ Core
assets: []
dependencies: [b4_ranges, b5_ranges, b6_errors_contracts, b7_build_tooling, b8_perf_layout, b9_concurrency, b10_resources, b11_footguns]
---

## Objective
Build a small, production-style library + sample app that integrates B4–B11: constrained APIs, safe resources, tested concurrency, measured performance, docs, CI, and packaging.

## Steps
1) Create `algo_utils` (header-only core + optional .cpp for demos).  
2) Add examples, docs, and end-to-end tests.  
3) Wire CI, packaging, and perf guards.  
4) Produce a releasable artifact with license/notice and version stamp.

## Smoke Test
- [ ] Fresh clone can: configure → build → test → docs → package on Linux/macOS/Windows.  
- [ ] Sample app runs a demo pipeline and prints version/build info.

## Notes
Prefer minimal dependencies; keep public headers clean and warning-free. Treat the docs as a contract—examples must compile.
