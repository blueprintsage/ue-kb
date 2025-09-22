---
id: niagara__performance__significance-lod__v1
family: niagara
topic: performance__significance-lod
version: 1
ue: ["5.3","5.4","5.5"]
status: stable
license: GPL-3.0-or-later
art_license: CC-BY
tags: ["lod","significance","bounds","series:sci-fi-vfx","part:3","source:book:butler"]
assets: []
deps: []
last_updated: 2025-09-21
---


# Performance — Significance & LOD


## Summary
Consistent emitter enable/disable and cost scaling by distance/importance.


## Buckets
- **Critical:** always on.
- **Near:** ≤ 25m.
- **Mid:** ≤ 50m.
- **Far:** 100m+ (no refraction, reduced collision).


## Budget Table
Per tier particle caps; document which emitters switch off by bucket.


## QA
Profile with crowds (10× instances) to catch emergent spikes.