---
title: F3/k25 — Pathfinding Property Harness & Benchmarks
kit_id: f3_pathfinding
version: 1.0
status: Draft
type: kata
---
## Objective
Fuzz/benchmark the pathfinding stack (A*, JPS, Theta*, HPA*, ARA*, D* Lite).
## Task
Generate random maps with fixed seeds and densities; assert optimality when expected, bounds for weighted/anytime; record expansions/time; export CSV summary.
## Acceptance
- [ ] Zero invariant violations across 10k trials; seeds logged.
- [ ] Benchmark table produced; chosen defaults justified by data.