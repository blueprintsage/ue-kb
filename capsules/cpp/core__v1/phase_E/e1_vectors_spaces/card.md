---
title: E1 — Vectors & Spaces
kit_id: e1_vectors_spaces
version: 1.0
status: Draft
category: Math
assets: []
dependencies: []
---

## Objective
Master dot/cross, projections, orthonormal bases, Gram–Schmidt, triple product, angles, barycentric coords, and basis changes.

## Steps
1) Dot/cross properties; magnitude/angle relations.  
2) Projections & rejections; component along/orthogonal.  
3) Orthonormal basis construction (Gram–Schmidt, robust).  
4) Change of basis and coordinate transforms.  
5) Barycentric coords for triangles; point-in-triangle test.

## Smoke Test
- [ ] Unit tests validate identities and numeric tolerances.  
- [ ] Basis vectors orthonormal within epsilon.

## Blueprint Hook
Arrays/vectors in BP: normalize, dot for FOV tests, cross for frame axes; Acceptance: simple view-cone filter works.