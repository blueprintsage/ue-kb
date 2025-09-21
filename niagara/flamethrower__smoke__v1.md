# Flamethrower — Smoke
**Domain:** niagara • **Level:** intermediate • **Engine:** UE5

## Recipe
- Second emitter `EM_Smoke` (CPU or GPU Sprite). Longer **Lifetime** (1.5–3s), larger **Size**.
- Velocity: inherit a portion of flame velocity, then add upward drift; **Drag** 0.2–0.4.
- Material: smoke flipbook (SubUV Life). **DepthFade** in material to avoid hard ground edges.
- Color Over Life: warm gray → cool gray; alpha fades last 25%.

## Checks
- Smoke lags flame, blooms wider, and dissipates gently.
## Pitfalls
- Gravity on will pull smoke down; leave off or very mild.
