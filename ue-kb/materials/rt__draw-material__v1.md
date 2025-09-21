# Render Target — Draw Material
**Domain:** materials • **Level:** intermediate • **Engine:** UE5

## Recipe
- Create **Render Target** (e.g., 1024²). Make a **BP_OffscreenDraw** with node **Draw Material to Render Target**.
- Feed a material (noise/pattern) into the draw each tick or via timer; output goes to the RT.
- Use the RT as a **Texture Parameter** in VFX materials or Niagara dynamic material.

## Checks
- RT updates in real time; swapping material input changes the on-card effect.
## Pitfalls
- Too frequent draws waste perf—prefer timer or event over tick when possible.
