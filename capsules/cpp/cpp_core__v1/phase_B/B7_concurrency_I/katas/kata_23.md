---
title: B7/k23 — Install rules & CMake package config
kit_id: b7_build_tooling
version: 1.0
status: Draft
type: kata
---
## Objective
Provide `install(TARGETS ...)` and export `ProjectConfig.cmake`.
## Acceptance
- [ ] `find_package(Project)` works in a separate sample; imported targets resolve on all OSes.
