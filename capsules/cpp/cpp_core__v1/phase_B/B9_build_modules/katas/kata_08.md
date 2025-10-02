---
title: B9/k8 — Reader–writer with shared_mutex
kit_id: b9_concurrency
version: 1.0
status: Draft
type: kata
---
## Objective
Implement many-readers/few-writers workload with `std::shared_mutex`.
## Acceptance
- [ ] Throughput improves over exclusive mutex for read-heavy ratio; correctness proven.
