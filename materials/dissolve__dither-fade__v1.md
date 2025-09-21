# Dissolve / Dither Fade
**Domain:** materials • **Level:** beginner→int • **Engine:** UE5

## Goal
Clean fade-outs without alpha-pop or sorting pain.

## Setup
- Material: **Translucent** or **Masked** (masked is cheaper if look allows).
- Inputs: `BaseColor`, `Normal`, `Emissive` (optional), `DissolveMask` (0–1), `EdgeWidth` (0–0.2), `EdgeColor`.

## Graph
1) **Threshold**: `T = saturate(TimeOrParam)` (use a scalar param or curve).
2) **Mask**: `Cut = step(DissolveMask, T)` (Masked) **or** `Opacity = smoothstep(T, T+EdgeWidth, DissolveMask)` (Translucent).
3) **Edge**: `Edge = smoothstep(T-EdgeWidth, T, DissolveMask) * EdgeColor * EdgeBoost`.
4) Final: `Emissive += Edge`, `Opacity` (if Translucent) or `Opacity Mask` (if Masked).

## Notes
- For filmic sparkle, swap step/smoothstep with **DitherTemporalAA** near the threshold.
- Drive `T` from Niagara (`User.Dissolve`) or Sequencer for precise timing.
