# Flipbook + DepthFade (Clean Intersections)
**Domain:** niagara • **Level:** beginner • **Engine:** UE5

## Recipe
- Texture: RGBA flipbook (e.g., 8×8).
- Material (Translucent): `Opacity = Saturate(Alpha) * DepthFade(Min,Max)`; `BaseColor = RGB`; (opt) multiply both by Particle Color.
- Niagara: Sprite renderer → **SubUV** on; **Subdivisions** set to grid; **Mode: Life**; **Interpolation: Linear**; **Loops: 1`.

## Tuning
- DepthFade: start Min 50–100 uu for big puffs (reduce for thin FX).
- Lifetime vs. cells: match so frames don’t rush or stall.

## Checks
- No halos against geometry; animation advances 0→end once and fades out near the tail.

## Pitfalls
- Masked blend kills soft edges; wrong cell order causes pops (ensure row-major).
