# First Sprite Emitter Setup
**Domain:** niagara • **Level:** beginner • **Engine:** UE5

## Recipe
- System: Template **Fountain** → `NS_FirstEmitter`.  
- Renderer: **Sprite**; material can be a flat debug color.  
- Spawn Rate 30–60; Lifetime 1.5–2.5s; Init Size 20–40; Init Velocity Z=50.  
- Color Over Life: start opaque → fade near end.
## Add-on Pack — First Texture & Additive
Import small sprite; additive material; spawn rate vs burst; size/color/alpha curves; gravity & collisions basics; loop tricks (seed, phase).
## Add-on Pack — First Texture & Additive
Import small sprite; set additive material; choose spawn **rate vs burst** based on read.
Shape over Life: size ↑, color bias curve, alpha ease-out.
Motion: basic gravity and simple collisions (kill on 2nd bounce).
Loop tricks: random seed/phase so repeats don’t sync; clamp lifetime for clarity.
## Checks
- Sprites appear, rise slightly, fade; Spawn Rate clearly changes density.
