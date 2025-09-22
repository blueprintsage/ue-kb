# /patterns/niagara__trail-lifetime-tuning__v1.md
---
title: "Pattern — Trail Lifetime Tuning"
id: pattern_trail-lifetime-tuning_v1
type: pattern
tags: ["pattern","niagara","trail","ribbon","remix:original"]
---
## Intent
Keep projectile trails readable without smearing or popping across speeds and frame rates.
## Steps (outline)
Width/opacity from lifetime curve → clamp stretch by speed → fade on stop → camera-distance bias.
## Acceptance
No over-stretch at >2× speed; fade completes <0.35s; readability at 5/15/30m.
