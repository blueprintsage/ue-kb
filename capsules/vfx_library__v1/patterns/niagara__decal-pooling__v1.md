# /patterns/niagara__decal-pooling__v1.md
---
title: "Pattern — Decal Pooling"
id: pattern_decal-pooling_v1
type: pattern
tags: ["pattern","decal","pooling","remix:original"]
---
## Intent
Reuse a small set of impact decals without hitching or leaks.
## Steps (outline)
BP pool actor → pre-spawn N decal comps → rotate through on impact → timed fade → return to pool.
## Acceptance
Pool never grows after warmup; 0 alloc spikes; 120 s soak = 0 leaks.
