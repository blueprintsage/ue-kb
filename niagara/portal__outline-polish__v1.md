# Portal — Outline Polish
**Domain:** niagara • **Level:** intermediate • **Engine:** UE5

## Recipe
- From `NS_Portal` rim: add **Color Over Life** (radial gradient via `Particle Color * Curve`).
- **SubUV spark layer**: tiny burst emitter on a circle, low Spawn Rate, short Lifetime (0.15–0.3s).
- **DepthFade** in rim material; add very soft **UV pan/distort** for shimmer.
- Optional: **User.Float Radius** (BP) that sets Shape Location radius and scales width.

## Checks
- Rim breathes subtly; random micro-sparks pop along the ring; radius animates smoothly.

## Pitfalls
- Overbright emissive blooms to white—cap with a mild clamp or lower exposure.
