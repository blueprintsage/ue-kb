---
title: B1/k25 — Sanitizers & Static Analysis (Baseline)
kit_id: b1_fundamentals_I
version: 1.0
status: Draft
type: kata
---
## Objective
Establish a baseline CI config with ASan/UBSan + clang‑tidy.
## Tasks
- Add CMake options to enable sanitizers; run clang‑tidy (modernize/readability) clean.
## Acceptance
- [ ] All B1 katas pass with sanitizers on; tidy has zero high‑severity warnings.