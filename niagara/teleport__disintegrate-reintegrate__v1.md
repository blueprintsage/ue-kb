# Teleport — Disintegrate/Reintegrate
**Domain:** niagara • **Level:** intermediate • **Engine:** UE5
## Recipe
- Out phase: mesh particles pulled upward (Cross with Up + Curl), alpha dither out.
- In phase: reverse—spawn from ring inward; fade in via mask.
## Checks
- Out → pause → In loop feels seamless with sound cue.
## Pitfalls
- Timing mismatch between mesh and sprite layers → visible pop.
