---
id: shared__qa__fx-checklist__v1
family: shared
topic: qa__fx-checklist
version: 1
ue: ["5.3","5.4","5.5"]
status: stable
license: GPL-3.0-or-later
art_license: CC-BY
tags: ["qa","perf","integration","series:sci-fi-vfx","part:3","source:book:butler"]
assets: []
deps: []
last_updated: 2025-09-21
---
## Add-on: Readability Rubric (Gnomon/Fundamentals)
- **Gameplay:** primary read clear at Near/Mid/Far; tails don’t hide gameplay.
- **Timing:** anticipation → impact → settle present and distinct.
- **Shape/Contrast:** bold silhouette; grayscale pass reads; emissive clamps respected.
- **Color:** hue separation from background; presets consistent across biomes.


# FX QA Checklist — Ship Safe


## Summary
Final gates for visual, performance, and integration readiness.


## Gates
- **Frame Budget:** record at 1080p/60; list target ms per sequence.
- **Memory:** atlas cap; check streaming pool warnings.
- **Network:** replication off by default; log spawns in DEV builds.
- **Accessibility:** emissive brightness bounds; colorblind‑safe team hues.