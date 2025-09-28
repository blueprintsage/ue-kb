# /bp/vfx-lib__spawn-router__v1.md
---
title: "VFX Library — Spawn Router"
id: vfx-lib_spawn-router_v1
type: lesson
tags: ["lesson","bp","router","datatable","remix:original"]
---
## Overview
A Blueprint that maps gameplay tags → effect rows → spawns the right Niagara system with parameters.
## Learning Goals
- Single entrypoint for FX spawning.
- Data-driven; easy to add new FX.
## Prerequisites
BP DataTables; gameplay tag basics.
## Steps (outline)
DataTable schema → Router BP switch on tag → spawn + set user params; log once on missing rows.
## QA Checklist
Zero hard refs; graceful failure; deterministic spawn order.
## Release Notes
v1.0 — router and schema defined.
