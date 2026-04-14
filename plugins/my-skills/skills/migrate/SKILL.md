---
name: migrate
description: Write a database migration — use when the user asks to create a migration, alter a schema, add or remove a column, change the database structure, or write an up/down migration.
---

# Database Migration

Write a database migration for the schema change described.

Include:
1. **Up migration** — the forward change
2. **Down migration** — the rollback
3. **Data migration** — backfill if existing rows need updating
4. **Index changes** — add/drop indexes affected by the schema change
5. **Safety check** — is this safe to run on a live DB? Locking risks? Table size?

Rules:
- Never DROP COLUMN or DROP TABLE without a deprecation migration first
- Always add NOT NULL columns with a default, then remove the default in a follow-up
- Test the down migration — it must actually work
- Note estimated lock duration for large tables
