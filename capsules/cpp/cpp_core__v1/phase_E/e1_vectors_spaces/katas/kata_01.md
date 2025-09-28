---
title: E1/k1 — Dot & Angle
kit_id: e1_vectors_spaces
version: 1.0
status: Draft
type: kata
prereq: []
---

## Objective
Compute angle between two vectors using the dot product, robustly clamped to [-1,1].

## Task
Given non‑zero `a,b∈R^3`, compute `θ = arccos( clamp(dot(a,b)/(‖a‖‖b‖), -1, 1) )` (radians & degrees).

## Acceptance
- [ ] `θ(a,b)` equals analytical angles for test pairs within 1e-6 rad.
- [ ] Handles nearly parallel/antiparallel inputs without NaNs.
- [ ] Zero‑length input triggers a safe error path.

## Hints
Normalize with epsilon guard; compare cosθ against reference.

## Keep/Revert
KEEP: clamp before `acos`. REVERT: naive `acos` on un‑clamped cosθ.