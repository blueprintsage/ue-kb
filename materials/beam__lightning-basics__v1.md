---
id: niagara__beam__lightning-basics__v1
family: niagara
topic: beam__lightning-basics
version: 1
ue: ["5.3","5.4","5.5"]
status: stable
license: GPL-3.0-or-later
art_license: CC-BY
source: []
tags: ["beam","lightning","ribbon","series:sci-fi-vfx","part:2"]
assets: []
deps: ["materials__beam__core-shell-fresnel__v1"]
last_updated: 2025-09-21
---


# Beam / Lightning — Basics (Niagara)


## Summary
Lightning arc using a ribbon over a spline with per‑segment jitter and flicker. Binds color/intensity to beam material instances for consistent look.


## System
- System: `NS_Lightning` · Emitter A: CPU Ribbon
- User Params: `BeamColor`, `BeamIntensity`, `ArcLength`, `FlickerRate`


## Walkthrough
1. Spawn N control points along spline; set tangents for slight bends.
2. Update: offset each segment with small noise; animate offset with time.
3. Add per‑segment flicker (random phase) to emissive scale.
4. Optional Emitter B: short‑lived sparks at start/end contact points.


## Determinism & Warmup
For cinematics, use fixed tick with a brief warmup; otherwise burst‑driven is fine.


## QA
Bounds must cover the entire arc even when jittered; disable view‑aligned normals if using custom normals.
- Added segmented jitter method and endpoint sparks; clarified deterministic setup.