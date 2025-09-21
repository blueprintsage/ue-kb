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
