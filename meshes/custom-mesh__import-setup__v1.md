# Custom Mesh — Import & Setup (for Niagara)
**Domain:** meshes • **Level:** beginner • **Engine:** UE5

## Recipe
- Import FBX: set **Import Uniform Scale** to match cm units; generate **Nanite** off (for particles) unless tiny counts.
- Create LODs or use simple low-poly; enable **Use Full Precision UVs** if distorted.
- For **Mesh Renderer** in Niagara: pick mesh, set **Facing Mode = Velocity**, randomize **Scale/Rotation**.
- Material: support **Vertex Color** (tint from Niagara).

## Checks
- Mesh particles face travel direction and vary in size; perf holds at target counts.
## Pitfalls
- Heavy meshes + lit materials crush perf—prefer unlit or simple lit and small triangles.
## Preset: Icicle (Maya → UE)
- **Modeling tips:** keep tip ≥ 2–3 cm radius to avoid subpixel shimmer; add 1 support loop near tip.
- **Normals/UVs:** harden seams along edges; UV island lengthwise; texel ~256–512px/m.
- **Export (FBX):** Smoothing Groups ON, Tangents/Normals ON, Units centimeters.
- **Import:** Combine Mesh OFF, **Build Nanite OFF** (unless hero mesh), Import Normals & Tangents.
- **Version notes:** 5.1–5.2 Nanite translucency is limited—prefer non-Nanite for translucent ice.
## Preset: Projectile Mesh (Capsule/Orb)
- **Capsule:** unit height for predictable `FX_Scale`; UV0 along length, UV1 radial cracks.
- **Import:** Import Normals & Tangents; Nanite OFF for translucent; pivot at muzzle centerline.
## Add-on Pack — Icicle, Shield, AOE Cylinder
Icicle: tip ≥2–3 cm; UV lengthwise; Import Normals & Tangents; Nanite OFF for translucent.  
Shield: quad/ico-sphere, even density; pivot center; Nanite OFF for translucent (5.1–5.3).  
AOE Cylinder: unit height/radius for predictable Scale; two UV sets (cap/rim); LOD1 for distant shots.
Projectile (Capsule/Orb): unit height; UV0 along length, UV1 radial cracks; pivot at muzzle centerline; Nanite OFF for translucent.
## Add-on Pack — Characters Setup (Stylized)
Import skeletal meshes with uniform texel density (~512–1024 px/m for close shots).
Pivot sanity (feet @ 0,0,0; forward +X). Create `MI_Char_Outline` (post-process or shell) gated by quality.
Attach sockets: `Muzzle_R`, `Hand_R`, `Spine2_Center` for FX tests; store in a `SK_Stylized_Test` rig.
## Add-on Pack — Houdini Mesh Prep → UE5
Low→mid poly primitives for FX (capsule/orb/shards); UVs: UDIM not required; keep seams hidden along long axis.
Export: scale 1.0, Z-up→Y-up fix as needed; name with unit suffix (`_u1m`, `_u50cm`).
Normals/Tangents: export from DCC; in UE set Import Normals & Tangents for consistency with stylized shading.
