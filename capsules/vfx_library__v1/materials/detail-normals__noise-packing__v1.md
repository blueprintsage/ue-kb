# Detail Normals & Noise Packing
**Domain:** materials • **Level:** intermediate • **Engine:** UE5
## Goal
Sharper surfaces and cheaper masks.
## Recipe
- Pack masks into **RGBA** of one texture (e.g., R=dirt, G=edges, B=wet, A=AO). Use **BC7/BC5** wisely; normal in BC5.
- Blend **Detail Normal** in world-space scale: `N = Normalize(BlendAngleCorrectedNormals(BaseN, DetailN * DetailStrength))`.
- Use cheap noise: tileable 2D noise + panners; avoid multiple heavy 3D noises; pre-bake where possible.
## Tips
- Drive mask strengths from **VertexColor** or MPC; preview cost with Material Stats and Quad Overdraw.
