# Ribbon — Polish Trails
**Domain:** niagara • **Level:** intermediate • **Engine:** UE5
## Recipe
- Spawn per unit on a moving source; set **RibbonID** stable; add **Tangent from Velocity**.
- Width over distance: wide at head → taper tail; color/alpha over age with subtle noise.
- **UVs:** V by distance, U by age for forward scroll; add jitter to break banding.
## Tips
- Clamp max ribbon points; fix bounds; test in Shader Complexity & Quad Overdraw.
- For impact bursts, cut lifetime short (0.15–0.4s) and sharpen width curve.
