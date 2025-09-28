---
title: G3 — Evaluation & Tuning
kit_id: g3_eval_tuning
version: 1.0
status: Draft
category: PCG
assets: []
dependencies: []
---

## Objective
Measure, tune, and regress‑test PCG outputs so changes are intentional and improvements are evidence‑based.

## Steps
1) **Connectivity:** flood‑fill components, articulation points, unreachable targets.  
2) **Layout metrics:** coverage, linearity, branching.  
3) **Pacing:** difficulty curve with rest pockets.  
4) **Sweeps:** parameter heatmaps; export CSV.  
5) **Search:** simple genetic tuner (GA) for parameters.  
6) **Runtime:** budget & caching.  
7) **Regression:** seeds + golden CSV/images; diff on change.

## Smoke Test
- [ ] All metrics compute without NaNs; stable across seeds.  
- [ ] Regression suite passes on saved seeds.