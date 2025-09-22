---
id: materials__vertex-paint__master-flow__v1
family: materials
topic: vertex-paint__master-flow
version: 1
ue: ["5.3","5.4","5.5"]
status: stable
license: GPL-3.0-or-later
art_license: CC-BY
tags: ["vertex-paint","heightlerp","series:sci-fi-vfx","part:3","source:book:butler"]
assets: []
deps: []
last_updated: 2025-09-21
---


# Vertex Paint — Master Flow


## Summary
Predictable vertex channel usage and blending for level art.


## Channels
R=height blend · G=detail scale · B=emissive mask · A=roughness offset.


## Notes
Normalize paint so R+G+B ≤ 1; clamp in material to avoid overshoot. Test Lumen GI stability with changing emissive.