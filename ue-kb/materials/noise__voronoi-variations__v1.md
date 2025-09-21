# Voronoi Noise — Variations
**Domain:** materials • **Level:** intermediate • **Engine:** UE5

## Recipe
- Build or sample **Voronoi**: outputs cell distance + cell ID. Create function `MF_Voronoi` with `Scale`, `Jitter`, `EdgeWidth`.
- Variants: **Cells** (distance), **Edges** (1 - smoothstep on distance), **Ridges** (abs derivatives).
- Use for masks, crackle emissive, or UV warps (convert height to normal for refraction).

## Checks
- Scale zooms pattern predictably; jitter changes irregularity; edges remain crisp.
## Pitfalls
- Tiling seams: blend two scales or rotate UVs slightly and add.
