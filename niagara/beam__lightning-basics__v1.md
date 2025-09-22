# Beam / Lightning — Basics
**Domain:** niagara • **Level:** intermediate • **Engine:** UE5
## Recipe
- Emitter: CPU **Beam** with points along a spline (or Spawn Per Unit on a moving source).
- Add **Noise** to beam tangent; jitter position per point; width taper over length.
- Renderer: **Ribbon** or **Beam**; UV: U=age, V=length; material uses core+shell (see beam material).
## Setup: Beam Emitter (Player → Target)
- **Emitter:** Beam type with Source/Target modules; default from player socket (e.g., `hand_r`) to hit location.
- **Jitter/Noise:** low-frequency noise for arc wobble; clamp amplitude by distance so short beams don’t over-bend.
- **Material (beam core/shell):** core = tight emissive band; shell = wider falloff with fresnel. Use Width from curve.
- **Collision tap:** line trace each tick → update Target → if blocking hit, route `FX.Electric.Hit`.
## Add More Elements
- **Forks:** secondary beams at 10–25% length, lower intensity, lifetime ≤0.12 s.
- **Glow sprite:** additive billboard at source/target with brief pulse.
- **Ground sparks:** see **Hit Impact — Sparks & Debris → Electric Sparks** variant.
## Add-on: Flipbook Lightning Support
- **Texture:** small 8–16f lightning sheet; animate via Sub-UV on tip sprites/forks.
- **Noise UV crawl (5.1):** switch to world-space panners or reduce speed to avoid shimmer.
## Add-on Pack — Player Beam & Forks
Source→Target from player socket; noise wobble clamped by distance; core/shell materials; forks at 10–25% length; tip sprites at ends; capture tip: key BeamActive on whole frames, no MB for clarity.
## Improve Effect
- Clamp beam width with distance; add camera-distance bias to emissive; expose `BeamColor`, `BeamWidth`, `ForkRate` as user params.
## Add-on Pack — Player Beam, Forks & Flipbook Lightning
Source→Target from player socket; noise wobble clamped by distance; core/shell materials; forks at 10–25% length; tip sprites at ends.
Flipbook lightning: 8–16f sheet on tip/forks via Sub-UV.
UE 5.1 note: if noise UVs crawl/shimmer, prefer world-space panners or reduce scroll speed.
## Version notes
- Tested 5.1/5.3/5.4. If noise UVs “crawl” in 5.1, switch to world-space panning or reduce speed.
## Checks
- Stable start/end; subtle jitter; width/brightness taper to tip.
## Pitfalls
- Too-few points → angular kinks; mismatched UVs → texture crawl.
