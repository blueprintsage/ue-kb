# PAT: SubUV by Age
**Purpose:** Animate flipbook frames over each particle’s lifetime.  
**Chain:** Renderer(Sprite SubUV) → SubUV Animation: `X,Y` cells • Mode: **Life** • Interp: **Linear** • Loops: **1**.  
**Params:** Lifetime matches perceived fps; optional user float to scale frame rate.  
**Checks:** Smooth 0→end playback; no popping (row-major cell order).  
**Pitfalls:** Blurry cells (try No Mips / bigger source), wrong grid dims.
