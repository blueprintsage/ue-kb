# UV Manipulation — Pan/Distort
**Domain:** materials • **Level:** beginner • **Engine:** UE5

## Recipe
- Base: `TextureSample(RGBA)` for your sprite/flipbook.
- Pan: `Panner` → offset UVs slowly (e.g., SpeedX 0.05, SpeedY 0.0) → plug to Texture’s **UVs**.
- Distort: sample a normal/noise → `Multiply` by small scalar (0.01–0.03) → `Append` with 0 → add to UVs before the Texture.
- Fade: keep your existing **Opacity = Saturate(A) * DepthFade**; tint via Particle Color.

## Checks
- Subtle drift/warp over time; no swimming at edges.

## Pitfalls
- Too-strong offsets cause stretching; clamp values and test against thin sprites.
