# /niagara/sequencer__shot-tracks-render__v2.md
---
title: "Sequencer — Shot, Tracks & Render (Unified)"
id: sequencer_shot-tracks-render_v2
type: lesson
tags: ["lesson","niagara","sequencer","camera","tracks","render","unified","remix:original"]
---
## Overview
Plan and capture VFX with Sequencer: set up a shot, drive Niagara via tracks/events, and render clean footage with Movie Render Queue (MRQ)—repeatable and color-consistent.
## Learning Goals
- Shot setup: cameras, focal/tone mapping guards, and exposure lock.
- Niagara control: Activate/Deactivate, user params, and event triggers on timeline.
- MRQ basics: presets, anti-aliasing, and color management that matches viewport intent.
## Prerequisites
UE5 Sequencer basics; at least one Niagara system to animate.
## Steps (outline)
1) **Shot Prep**: CineCameraActor → focal length/aperture → exposure **Manual**; lock WB if needed.  
2) **Niagara Tracks**: Add Track → Niagara Component → key **Activate** peaks; add **User Parameter** tracks (e.g., Intensity/Color).  
3) **Events**: Add BP track with keyframes to call Router tags (e.g., `FX.Muzzle.Fire`, `FX.Impact.Hit`).  
4) **Timing**: Use sub-sequences for beats; keep FX events on whole-frame timestamps; add pre-roll if warmup needed.  
5) **Render (MRQ)**: Pick preset → Temporal AA high; output EXR/PNG; disable motion blur for readability shots; clamp tone mapper if color shifts.  
6) **Sanity Pass**: Play-in-editor at 60/120 fps; verify readbacks match render.
## Add-on: Projectile Beats (Anticipation → Climax → Settle)
- **Keys:** pre-key muzzle (anticipation), align trail start to frame, impact on whole frame, settle tail 0.3–0.8 s.
- **MRQ:** turn motion blur OFF for readability passes; clamp highlights on muzzle/impact spikes.
## Add-on Pack — Preroll, Beats, Cinematic Tips
Preroll 2–4 s for loops; Activate/Deactivate on whole frames; lock exposure/WB.  
Timing beats: Anticipation → Impact/Climax → Settle; sub-sequences for clean edits.  
Beam capture: key BeamActive; no MB; clamp highlights.  
Fire/Explosion: emissive spike for 2–4 frames; tone-mapper clamp; smoke preroll.  
Fog/Env: continuity across shots (same seed/key times).  
> Tip: For frosty camera hits, see Decals → Frost Overlay.

## Post FX: Ice Attack Grade
- Lock exposure; cool white balance slightly; subtle bloom (threshold high, intensity low).
- Optional LUT: gentle blue lift in mids; avoid crushing blacks to keep read.
- Version notes: 5.1 MRQ tone-mapper → use **Cinematic** preset; in 5.3+ default preset matches viewport better.
> Tip: For a brief frosty screen hit on heavy impacts, see **Impact Decals — Spawn & Polish (Unified) → Optional: Frost Overlay**.
## Tip: Beam Capture
- For readability shots, key `BeamActive` on/off on whole frames; render with motion blur off; clamp exposure so fork detail isn’t crushed.
## QA Checklist
FX timing matches keys; no exposure breathing; rendered color close to viewport; no dropped events; MRQ output plays cleanly at target fps.
## Release Notes
v2 — merged “Sequencer Hooks — Tracks & Control” with beginner course notes; added router + MRQ preset tips.
## Version notes
- Tested 5.1/5.3/5.4.  
- 5.1 MRQ tone-mapper mismatch: use **Cinematic** preset, lock exposure, disable auto exposure.  
- If Niagara doesn’t obey Activate keys: ensure you’re keying the **component** track and not the asset; toggle `Reset On Seek` off for persistent sims.
