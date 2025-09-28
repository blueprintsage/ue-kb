---
title: E5/k3 — Cubic Hermite (Endpoint Tangents)
kit_id: e5_extras_splines_noise
version: 1.0
status: Draft
type: kata
---
## Objective
Implement cubic **Hermite** interpolation with endpoint tangents m0,m1.
## Task
Evaluate H(t)=h00 p0 + h10 m0 + h01 p1 + h11 m1 with h00=2t^3−3t^2+1, h10=t^3−2t^2+t, h01=−2t^3+3t^2, h11=t^3−t^2; verify endpoint position/tangent.
## Acceptance
- [ ] H(0)=p0, H(1)=p1, H'(0)=m0, H'(1)=m1 within 1e-7.
- [ ] Monotone segment preserves monotonicity when slopes clamped.
## Keep/Revert
KEEP: optional Fritsch–Carlson slope clamp for monotone data. REVERT: overshoot allowed on monotone samples.