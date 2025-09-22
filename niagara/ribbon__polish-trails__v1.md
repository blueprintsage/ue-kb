---
id: niagara__ribbon__polish-trails__v1
family: niagara
topic: ribbon__polish-trails
version: 1
ue: ["5.3","5.4","5.5"]
status: stable
license: GPL-3.0-or-later
art_license: CC-BY
tags: ["ribbon","trails","uv","series:sci-fi-vfx","part:3","source:book:butler"]
assets: []
deps: []
last_updated: 2025-09-21
---


# Ribbon — Polish Trails


## Summary
Stable, readable trails with clean UVs and minimal aliasing at distance.


## UV Policy
- **UV0:** distance‑along‑trail for textures.
- **UV1:** normalized age (0→1) for dissolve/width.


## Stability
- Smooth tangents; clamp max per‑frame turn to prevent kinks.
- Minimum width ≈ **1.25 px at 1080p**; TAAU recommended for ultra‑thin.


## QA
Fast camera pans; check TAA ghosting; verify trail end culling.