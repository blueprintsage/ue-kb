---
id: materials__viewport__cost-debugging__v1
family: materials
topic: viewport__cost-debugging
version: 1
ue: ["5.3","5.4","5.5"]
status: stable
license: GPL-3.0-or-later
art_license: CC-BY
tags: ["perf","viewmodes","stats","series:sci-fi-vfx","part:3","source:book:butler"]
assets: []
deps: []
last_updated: 2025-09-21
---


# Viewport Cost Debugging


## Summary
Quick triage for material/VFX performance using built‑in viewmodes and captures.


## Viewmodes
Shader Complexity · Quad Overdraw · Material Complexity.


## Heuristics
- Background sprites ≤ **60 ALU**, ≤ **2** texture lookups.
- Beams ≤ **80 ALU**; refraction sparingly.


## Capture Script
Editor utility cycles viewmodes and saves thumbnails per effect.