# Vertex Paint — Master Flow
**Domain:** materials • **Level:** beginner→int • **Engine:** UE5
## Setup
- Mesh with **Vertex Color**; in Material, sample **VertexColor.r/g/b/a** to blend layers (e.g., clean→dirty, moss, edge wear).
- Use `HeightLerp` (or height masks) for clean transitions; normalize/pack masks to reduce samplers.
## Workflow
- Paint in Mesh Paint mode (Shift+2): set brush strength/flow; paint R/G/B as layers.
- When happy: **Apply to Source** (if needed), save LODs; expose scalars to tweak blend strength in instances.
