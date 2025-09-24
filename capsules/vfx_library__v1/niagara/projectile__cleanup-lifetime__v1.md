# /niagara/projectile__cleanup-lifetime__v1.md
---
title: "Projectile — Cleanup & Lifetime"
id: projectile_cleanup-lifetime_v1
type: lesson
tags: ["lesson","niagara","cleanup","lifetime","pooling","remix:original"]
---
## Overview
Guarantee FX stop when the projectile dies or exits play—no orphaned systems.
## Learning Goals
- Lifetime budget enforced via params.
- Pool or soft-kill on stop.
## Prerequisites
Niagara module stacks; BP destroy flow.
## Steps (outline)
Lifetime param → auto-kill modules → OnDestroyed soft-kill; optional pooled systems.
## QA Checklist
Zero leaks after 5 min soak; pooled FX never exceed cap.
## Release Notes
v1.0 — cleanup path established.
