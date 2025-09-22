# /niagara/projectile__core-materials__v1.md
---
title: "Projectile — Core Materials"
id: projectile_core-materials_v1
type: lesson
tags: ["lesson","niagara","materials","projectile","remix:original"]
---
## Overview
Author a readable projectile core with core/shell emissive, fresnel rim, and optional distortion—built as reusable material functions.
## Learning Goals
- Core→shell layering with tunable brightness and radius.
- Param sweep that holds shape from 5–30m and in motion blur.
## Prerequisites
UE5 materials basics; Niagara familiarity.
## Steps (outline)
MF_CoreGlow → MF_ShellFresnel → combine in M_ProjectileCore → MI variants; expose Color/Intensity/Radius.
## QA Checklist
No overbright clipping; refraction optional/off on low preset; LODs stable.
## Release Notes
v1.0 — first pass functions + instance setup.
