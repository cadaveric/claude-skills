---
name: perf
description: Performance audit — use when the user asks to optimize, profile, improve performance, speed something up, fix slow code, or reduce latency.
---

# Performance Audit

Profile and optimize the current file or the system described.

Steps:
1. Identify the critical path (what the user is waiting for)
2. Find the bottlenecks: N+1s, blocking calls, missing indexes, redundant work
3. Propose fixes in order of impact (biggest win first)
4. For each fix: estimated improvement, risk of regression, how to verify

Rules:
- Never optimize without measuring first — cite or describe how to measure
- Premature micro-optimization is worse than no optimization
- Cache invalidation must be explicit — describe when/how each cache clears
- Async is not always faster — explain the concurrency model change if proposing it
