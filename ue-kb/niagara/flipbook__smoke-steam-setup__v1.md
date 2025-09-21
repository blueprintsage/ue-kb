# Smoke/Steam Flipbook Setup
**Domain:** niagara • **Level:** beginner • **Engine:** UE5  
**Objective:** Render smoke/steam sprites with a flipbook and clean edges.

## Recipe
- Texture: RGBA flipbook (e.g., 8×8). Import → (opt) No Mipmaps if blurry.
- Material: Translucent → `Opacity = Alpha * DepthFade` (Clamp), `BaseColor = RGB`; (opt) multiply by Particle Color.
- Niagara: Sprite renderer → **SubUV** on; **Subdivisions** X=8 Y=8; **Mode: Life**; **Interpolation: Linear**; **Loops: 1**.
- Starter tuning: Lifetime 2.5–3.5s; Spawn Rate 40–60; Init Velocity Z 30–50; Drag 0.2–0.4; Color Over Life dark→light.

## Checks
- Frames advance 0→end once; last 20% fades out.
- No halos at intersections (DepthFade tuned).
