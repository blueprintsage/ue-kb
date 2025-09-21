# First VFX Material (Sprite)
**Domain:** materials • **Level:** beginner • **Engine:** UE5  
**Objective:** Build a clean translucent sprite material for flipbooks/smoke.

## Recipe
- **Material**: Domain = Surface; **Blend = Translucent**; Shading = **Unlit** (consistent look).  
  *(If you need scene lighting, use Default Lit and keep Opacity the same.)*
- **TextureSample (RGBA)** → (optional) **SubUVFunction** to drive UVs from Niagara.
- **Opacity**: `Saturate( Alpha ) * DepthFade(Min,Max)` → **Opacity**. Start Min 50–100uu for big puffs.
- **Color**: Unlit → **Emissive Color = RGB**. *(Lit: Base Color = RGB.)*
- **Tint/Fade from Niagara**: multiply RGB and Opacity by **Particle Color**.
- **Opaque plates fix**: if art lacks alpha, use `Luminance(RGB)` → remap `Saturate((L-0.15)/0.5)` as Opacity.

## Checks
- No halos at intersections (tune DepthFade).  
- Particle Color tint/fade works from Niagara.

## Pitfalls
- Masked blend removes soft edges.  
- Forgetting to clamp before DepthFade causes blowouts.
