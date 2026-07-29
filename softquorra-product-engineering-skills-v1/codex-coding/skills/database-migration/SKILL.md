---
name: database-migration
description: Implements an approved database/schema migration and backfill safely using the repository's existing ORM/migration tooling. Use for PostgreSQL, Prisma, schema changes, indexes, constraints, tenant migrations, data backfills, or compatibility migrations.
metadata:
  author: softquorra
  version: "1.0"
---

# Database Migration

## Goal
Change production data structures without unnecessary data loss, downtime, or compatibility risk.

## Workflow
1. Read the approved data/migration plan and inspect current schema/migration conventions.
2. Classify the change as additive, backfill, constraint, rename, or destructive.
3. Verify compatibility assumptions and deployment order.
4. Prefer expand → migrate/backfill → contract for risky live changes.
5. Implement schema migration and a controlled backfill when needed.
6. Add constraints only after existing data is valid where required; add indexes from justified access patterns.
7. Verify tenant/data ownership and migration idempotency/restart behavior where applicable.
8. Run migration/schema/tests and document rollback or forward-fix strategy.

## Output
- Migration files
- Data impact
- Backfill plan/result
- Compatibility/deploy order
- Validation
- Rollback/forward-fix

## Quality / Guardrails
- Stop if the change can lose production data without explicit approval.
- Stop if backfill scale/locking risk is unknown and material.
- Do not violate tenant isolation.
