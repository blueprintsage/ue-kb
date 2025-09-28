---
id: materials__respawn-energy-base__v1
family: materials
topic: respawn-energy-base
version: 1
ue: ["5.3","5.4","5.5"]
status: draft
license: GPL-3.0-or-later
art_license: CC-BY
source:
- type: course
slug: sci-fi-vfx
part: part-1
tags: ["level:201","series:sci-fi-vfx","part:1","pack:sci-fi"]
assets: []
deps: []
last_updated: 2025-09-21
---


# Respawn — Energy Base (Materials)


## Summary
Scrolling energy base material for platform foundation.


## Setup
- Project material folder + instance workflow.
- Texture import settings; tiling & panning.


## Steps
1. Create master `M_Respawn_EnergyBase` with panner + mask.
2. Expose speed/tiling/intensity as params; create MI for tuning.


## Performance — Viewport Cost Debugging
- Use shader complexity view.
- Keep ops minimal; prefer LUTs for curves.


## QA Checklist
- No runtime expensive nodes; instances only.
- Parameters documented; defaults sane.


## Links
- Cross-ref: `niagara__respawn-platform-energy-base__v1`.