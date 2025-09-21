# Beam / Lightning — Basics
**Domain:** niagara • **Level:** intermediate • **Engine:** UE5
## Recipe
- Emitter: CPU **Beam** with points along a spline (or Spawn Per Unit on a moving source).
- Add **Noise** to beam tangent; jitter position per point; width taper over length.
- Renderer: **Ribbon** or **Beam**; UV: U=age, V=length; material uses core+shell (see beam material).
## Checks
- Stable start/end; subtle jitter; width/brightness taper to tip.
## Pitfalls
- Too-few points → angular kinks; mismatched UVs → texture crawl.
