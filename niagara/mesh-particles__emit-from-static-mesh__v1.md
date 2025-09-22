---
id: niagara__mesh-particles__emit-from-static-mesh__v1
family: niagara
topic: mesh-particles__emit-from-static-mesh
version: 1
ue: ["5.3","5.4","5.5"]
status: stable
license: GPL-3.0-or-later
art_license: CC-BY
tags: ["mesh","surface","inherit","series:sci-fi-vfx","part:3","source:book:butler"]
assets: []
deps: []
last_updated: 2025-09-21
---


# Mesh Particles — Emit From Static Mesh


## Summary
Surface‑accurate emission for shards/dust with predictable density and normals.


## Emission
- Sample mesh triangles by area; jitter barycentric coords to avoid banding.
- Optional: offset spawn along normal by small scalar for separation.


## Perf & Scalability
- Cap `ParticlesPerTriangle`; expose as scalability param.
- Re‑sample on LOD change or pin to a specific source LOD.


## QA
LOD transitions; verify normal orientation for lighting and velocity.