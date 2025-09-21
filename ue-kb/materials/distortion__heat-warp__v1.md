# Heat Distortion (Screen-Space Warp)
**Objective:** Add a refractive heat shimmer.
## Recipe
- Material: **Translucent**, **Unlit**, **Refraction** driven by a panning normal map (or noise → normal).
- Nodes: `Panner(0.1,0)` → `NormalFromHeightmap` (or sample a normal texture) → plug to **Refraction** (e.g., 0.02–0.06 scale).
- Niagara: sprite/mesh emitter with this material; fade alpha near edges (DepthFade if near geo).
## Checks
- Background warps behind particles; strength adjustable without artifacts.
## Pitfalls
- Too-strong refraction looks watery; keep values subtle and vary over life.
