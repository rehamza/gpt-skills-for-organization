---
name: data-api-implementation-plan
description: Creates implementation-level database, migration, and API/interface plans from approved requirements and existing repository conventions. Use for schema changes, entities, indexes, tenancy, endpoints, contracts, webhooks, backfills, compatibility, or API task planning.
metadata:
  author: softquorra
  version: "1.0"
---

# Data Api Implementation Plan

## Goal
Design safe data and interface changes that can be implemented incrementally.

## Workflow
1. For each entity identify domain owner, tenant boundary, lifecycle, sensitivity, conceptual fields, constraints, relationships, and access patterns.
2. Plan indexes from actual access patterns rather than speculation.
3. Classify migrations as additive/backfill/constraint/rename/destructive and define deployment order, compatibility, validation, rollback/forward-fix, and cleanup.
4. For each interface define consumer, purpose, auth/authz, request/response concept, validation, errors, idempotency, pagination/rate limits, side effects, audit/analytics, and compatibility.
5. For webhooks define verification, dedupe, ordering, queue processing, retries, and reconciliation.
6. Map data/API work to requirements and tests.

## Output
- Data entity/change plan
- Migration/backfill plan
- API/interface contracts
- Webhook plan where relevant
- Compatibility/rollback
- Tests and traceability

## Quality / Guardrails
- Follow existing repository conventions when known.
- Do not turn conceptual requirements into destructive migration steps without an approved rollout plan.
