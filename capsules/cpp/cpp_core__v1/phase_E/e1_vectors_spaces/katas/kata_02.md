---
title: E1/k2 — Cross & Triangle Area
kit_id: e1_vectors_spaces
version: 1.0
status: Draft
type: kata
---

## Objective
Use cross product magnitude to get twice the triangle area.

## Task
Given triangle (A,B,C), compute `area = 0.5 * ‖(B−A)×(C−A)‖`.

## Acceptance
- [ ] Matches Heron’s formula within 1e-6 on random triangles.
- [ ] Zero area for collinear points.

## Keep/Revert
KEEP: stable norm computation. REVERT: area from angles only.