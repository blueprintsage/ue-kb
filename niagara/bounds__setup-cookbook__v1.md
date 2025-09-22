---
id: niagara__bounds__setup-cookbook__v1
family: niagara
topic: bounds__setup-cookbook
version: 1
ue: ["5.3","5.4","5.5"]
status: stable
license: GPL-3.0-or-later
art_license: CC-BY
tags: ["bounds","culling","series:sci-fi-vfx","part:3","source:book:butler"]
assets: []
deps: []
last_updated: 2025-09-21
---


# Niagara Bounds — Setup Cookbook


## Summary
Fast, reliable bounds for cinematic bursts and gameplay loops. Avoids camera pop‑in and preserves perf.


## Heuristics
- **Burst FX:** `BoundsRadius ≈ MaxSpeed * Lifetime + SpawnRadius` then × **1.25** safety margin.
- **Trails/Ribbons:** project max sweep (speed × turn) and add camera look‑ahead.
- **Shockwaves:** use target max radius + 10%.


## Workflow
1. Author a `BoundsScale` user param (default 1.2). Bind to each emitter’s bounds override.
2. Set preview gizmos (spheres/boxes) in an Editor Utility Widget to visualize live bounds.
3. For cinematic shots: lock camera FOV tests at 18–24mm and 110°.


## Debug
- Enable bounds view and scrub timeline; look for edge culls.
- Log instances with `Significance < Near` that still spawn heavy emitters.