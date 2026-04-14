---
name: sql
description: Write or optimize SQL — use when the user asks to write a query, optimize a slow query, explain a query plan, or design a schema.
---

# SQL

Handle the SQL task described: write, optimize, explain, or review.

## Write

When writing a new query:
1. Start with the simplest correct query, then optimize
2. Use CTEs (`WITH`) for readability over nested subqueries
3. Prefer explicit JOINs over implicit (comma) joins
4. Always alias tables in multi-table queries
5. Use parameterized placeholders (`$1`, `?`, `%s`) — never string-interpolate user input

## Optimize

When given a slow query:
1. Ask for (or read) the `EXPLAIN ANALYZE` output
2. Identify the bottleneck: seq scan on large table, nested loop on wrong side, missing index, bad cardinality estimate
3. Propose fixes in order of impact:
   - Index additions (specify columns, partial/composite if beneficial)
   - Query rewrite (eliminate correlated subqueries, push filters earlier)
   - Schema change (denormalization, materialized view) — only if index/rewrite can't fix it
4. Show before/after `EXPLAIN` cost estimates if possible

## Review

Check for:
- N+1 patterns (query inside a loop)
- Missing indexes on JOIN/WHERE/ORDER BY columns
- `SELECT *` in production code
- Unparameterized inputs (SQL injection risk)
- Lock contention (UPDATE/DELETE without index on WHERE clause on large tables)

## Output

For each query: purpose, the SQL, and a note on indexes required for it to perform well.
