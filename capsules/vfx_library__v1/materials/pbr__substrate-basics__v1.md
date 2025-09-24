# PBR & Substrate — Basics
**Domain:** materials • **Level:** beginner→int • **Engine:** UE5
## Refresher
- Core PBR inputs: BaseColor, Normal, Metallic, Specular, Roughness, Emissive, Opacity(Mask).
- Keep values physically plausible (roughness 0.04–0.98, metallic 0/1 for most cases).
## Substrate (UE5)
- Use **Substrate** to blend layered lobes (e.g., clearcoat over paint) more physically.
- Start simple: one base BSDF + optional top lobe; watch instruction count; prefer Material Instances.
## Tips
- Tone-map safe emissive (avoid hard clipping); pack masks; preview in Material Stats.
