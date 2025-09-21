# FX QA Checklist — Ship Safe
**Domain:** shared • **Level:** all • **Engine:** UE5
## Visual
- No first-frame pops (warmup), no z-fighting at spawn, clean depthfade on translucent.
- Overdraw acceptable in Quad Overdraw; ribbons/sprites not full-screen for long.
## Performance
- Fixed bounds set; significance/LOD configured; tick and spawn rates scale down at distance.
- Materials: instruction count sane; texture taps minimized; no heavy per-pixel loops.
## Integration
- Niagara User params named consistently (`User.*`); BP hooks event-driven (no Tick spam).
- Sequencer cues align; sounds timed; multiplayer: client-safe spawns or server auth as needed.
