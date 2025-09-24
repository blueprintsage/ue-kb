---
id: niagara__shield__impact-ripple__v1
family: niagara
topic: shield__impact-ripple
version: 1
ue: ["5.3","5.4","5.5"]
status: stable
license: GPL-3.0-or-later
art_license: CC-BY
source: []
tags: ["shield","ripple","impact","series:sci-fi-vfx","part:2"]
assets: []
deps: []
last_updated: 2025-09-21
---


# Shield — Impact Ripple (Niagara)


## Summary
Localized ripple at the hit point on a spherical shield, with a small directional spark burst.


## System
- Emitter A (ripple): Camera‑facing quad spawned at impact; radius animated by curve; soft particles for intersection.
- Emitter B (sparks): CPU sprites launched along surface normal; short lifetime; small gravity.
- Material: normal‑mapped ring + emissive pulse; `TeamColor` user param.


## QA
Tight bounds per‑impact; handle concurrent impacts without culling each other.


---
## Sci‑Fi Batch 1 — Part 2 Additions (2025‑09‑21)
- Added spark burst and user‑param color control; refined bounds guidance.