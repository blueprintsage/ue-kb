# Mesh Particles — Emit From Static Mesh
**Domain:** niagara • **Level:** intermediate • **Engine:** UE5
## Goal
Spawn particles on a mesh surface and inherit its motion.
## Setup
- **Location:** Mesh Reproduction Sprite/CPU Events or **Location: Static Mesh Surface** (Surface Only + Triangle Area Weighting).
- **Inherit:** add **Inherit Velocity** (from parent actor) and random rotation/scale.
- **Motion:** Gravity + Drag; optional Curl for breakup; Mesh or Sprite renderer.
## Checks
- Even surface distribution; particles inherit motion on moving meshes; no clumping.
## Pitfalls
- GPU readers vs CPU events mismatch; make sure sim type matches your needs.
