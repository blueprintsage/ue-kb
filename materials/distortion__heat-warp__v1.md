# Heat Distortion (Screen-Space Warp)
**Objective:** Add a refractive heat shimmer.
## Recipe
- Material: **Translucent**, **Unlit**, **Refraction** driven by a panning normal map (or noise → normal).
- Nodes: `Panner(0.1,0)` → `NormalFromHeightmap` (or sample a normal texture) → plug to **Refraction** (e.g., 0.02–0.06 scale).
- Niagara: sprite/mesh emitter with this material; fade alpha near edges (DepthFade if near geo).
## Add-on Pack — Heat Haze, AOE Dissolve/Distort
Heat Haze: Perlin mask panner 0.03–0.06; Refraction 0.005–0.012 (gate by quality).  
AOE Dissolve: Ordered Dither or Temporal Dither; edge glow via fresnel mask; optional refraction 0.01–0.02 (Mid+).

## Checks
- Background warps behind particles; strength adjustable without artifacts.
## Pitfalls
- Too-strong refraction looks watery; keep values subtle and vary over life.
