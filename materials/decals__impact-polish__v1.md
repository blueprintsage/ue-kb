# Impact Decals — Polish
**Domain:** materials • **Level:** intermediate • **Engine:** UE5
## Material
- Deferred Decal; **Translucent**, **DBuffer Translucent Color / Normal / Roughness** as needed.
- Inputs: Albedo, Normal, Roughness, GrungeMask, EdgeSoftness.
- Fade: `Opacity = smoothstep(Edge, Edge+Softness, GrungeMask) * LifetimeFade`.
## Usage
- Spawn at hit with rot-from-normal; randomize scale/rotation; lifespan 10–90s.
- Avoid stacking: small size, clamp emissive, keep normal strength modest.
