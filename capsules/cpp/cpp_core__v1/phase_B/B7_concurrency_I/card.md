---
title: B7 — Build & Tooling (quality gates)
kit_id: b7_build_tooling
version: 1.0
status: Draft
category: C++ Core
assets: []
dependencies: []
---

## Objective
Make quality the default with reproducible builds, strict warnings, sanitizers, static analysis, formatting, docs, and CI—per target, not global.

## Steps
1) CMake hygiene: targets, options, features, config headers.
2) Warnings-as-errors & toolchains; per-target sanitizer/analysis toggles.
3) Static analysis (clang-tidy/IWYU), formatting, codegen visibility, and symbol hygiene.
4) Deterministic builds: ccache, SOURCE_DATE_EPOCH, version stamping.
5) CI with caches; packaging/install rules; reproducers.

## Smoke Test
- [ ] `configure && build && test
