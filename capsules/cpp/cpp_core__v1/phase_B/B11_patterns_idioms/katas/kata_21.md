---
title: B11/k21 — Temporary lifetime in range pipelines
kit_id: b11_footguns
version: 1.0
status: Draft
type: kata
---
## Objective
Pipe from a temporary and dangle; fix by materializing/owning or ensuring source lifetime.
## Acceptance
- [ ] Bad pipeline fails under sanitizers; fixed pipeline passes; rule added to README.
