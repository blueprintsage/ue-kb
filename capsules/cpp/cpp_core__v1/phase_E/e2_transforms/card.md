---
title: E2 — Transforms
kit_id: e2_transforms
version: 1.0
status: Draft
category: Math
assets: []
dependencies: [e1_vectors_spaces]
---

## Objective
Build and reason about transforms: matrices, quaternions, frames; composition, inversion, look-at, projections, and screen rays.

## Steps
1) Rigid transform compose/decompose (T * R * S).  
2) Quat normalize/multiply; from-axis/angle and from-matrix.  
3) LookAt matrix; camera frame.  
4) Perspective/orthographic projection; NDC mapping.  
5) Screen‑to‑world ray construction.

## Smoke Test
- [ ] Rigid inverse equals transpose/negated position.  
- [ ] Quat * v == R * v within epsilon.

## Blueprint Hook
BP: Compose transforms; `GetForwardVector`, build camera ray from screen; Acceptance: line trace from cursor hits expected.