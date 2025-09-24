---
title: BR12/k1 — Configure AIPerception (sight+hearing)
kit_id: br12_perception_hearing
version: 1.0
status: Draft
type: kata
---
## Goal
AI reacts to noise out of sight.
## Given
AI with AIPerception component.
## Task
Enable Sight and Hearing; register `OnTargetPerceptionUpdated`; on hearing, set `LastKnownLocation` and a short investigate flag.
## Acceptance
- [ ] Shooting (ReportNoiseEvent) triggers investigate when player is hidden.