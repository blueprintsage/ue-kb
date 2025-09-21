# Sub-UV Animation (Renderer Setup)
**Domain:** niagara • **Level:** beginner • **Engine:** UE5  
**Objective:** Animate flipbook frames over each particle’s lifetime.

## Recipe
- **Sprite Renderer**: enable **Sub UV**.  
  - **Subdivisions**: set **X** and **Y** to your grid (e.g., 8×8).  
  - **Interpolation**: **Linear**.  
  - **Mode**: **Life** (Age → Linear). **Loops**: 1.
- **Timing**: match particle **Lifetime** to the perceived frame rate; optionally scale with a user float.

## Checks
- Frames run smoothly from 0→end once; fade overlaps last frames.

## Pitfalls
- Wrong cell order (should be row-major).  
- Blurry frames → try No Mipmaps or larger source cells.
