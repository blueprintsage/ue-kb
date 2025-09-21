# Perlin Noise (Material Function)
**Domain:** materials • **Level:** beginner • **Engine:** UE5

## Recipe
- Create **Material Function** `MF_Perlin2D`.
- Inside: `TextureSample(Noise)` or build with `Simplex/Perlin` nodes if available; inputs: `UV`, `Scale` (float2), `Intensity`.
- Output: `(Noise(UV * Scale) * Intensity)` → return as `NoiseOut`.
- Use in materials: `MF_Perlin2D(UVs, float2(2,1), 1)` → drive Emissive/Opacity or UV distortion (convert to normal with `Derivative`→`NormalFromHeight` if needed).

## Checks
- Changing `Scale` zooms noise; `Intensity` scales effect predictably.

## Pitfalls
- Tiling artifacts: add a small secondary noise at a different scale and add/mix.
