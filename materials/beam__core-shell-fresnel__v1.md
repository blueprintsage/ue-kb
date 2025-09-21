# Beam Material — Core/Shell Fresnel
**Domain:** materials • **Level:** intermediate • **Engine:** UE5
## Recipe
- Unlit; Emissive = `(CoreTex * 2)` + `(ShellTex * Fresnel(Exp 4–8) * 1.5)`.
- Add **UV pan** forward; optional **glow mask** near start/end via V.
- Opacity = `Saturate(CoreAlpha + ShellAlpha)`.
## Checks
- Hot inner core, softer outer bloom; scroll reads forward.
## Pitfalls
- Overbright = white clip; clamp or tone-map friendly values.
