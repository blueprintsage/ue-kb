# Hologram — Scanline & Dither
**Domain:** materials • **Level:** intermediate • **Engine:** UE5
## Recipe
- Unlit translucent; Emissive = BaseTex * tint; overlay **scanline** (sin on V + pan).
- **DitherTemporalAA** node for flicker; optional depthfade + UV distort.
## Checks
- Soft flicker without hard popping; readable scanlines at mid distance.
## Pitfalls
- Overpowering flicker; keep amplitude subtle and rate <10 Hz.
