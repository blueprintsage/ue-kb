# Parallax & Height-Blend (Ground/Decals)
**Domain:** materials • **Level:** intermediate • **Engine:** UE5
## Goal
Depthy surfaces and clean transitions between two materials.
## Recipe
- Use **Parallax Occlusion Mapping** sparingly (few steps; clamp), or cheaper **Bump Offset** for distant shots.
- **Height-Blend:** `HeightLerp(A,B, Aheight, Bheight, Contrast)` for rock-into-sand, with optional world-aligned normals for continuity.
- Add **Macro variation** at large tiling; keep emissive low to avoid blown highlights.
## Checks
- Angle change shows convincing depth; blend line disappears under varied height.
