# SoftQuorra Data & API Planning Standard

# Data Planning

For each entity/change define:
- name;
- purpose;
- owner/domain;
- tenant boundary;
- lifecycle;
- sensitive classification.

## Schema
Conceptually define key fields, types, required/optional status, uniqueness, relationships, statuses, and timestamps/versioning where required.

Do not generate migration code unless asked in an implementation/coding step.

## Invariants
Examples:
- unique external provider ID per tenant;
- a child resource cannot reference another tenant;
- state transitions must follow approved rules.

Use DB constraints where appropriate.

## Indexes
Plan from actual access/query patterns: filters, joins, sort, uniqueness, and high-volume lookup. Avoid speculative indexes.

## Tenancy
Every tenant-owned record needs a reliable isolation strategy.

Plan tenant key, query enforcement, job context, cache key, storage path, and admin access.

## Migration
For each migration define:
- additive/destructive;
- compatibility;
- deploy order;
- backfill;
- validation;
- rollback;
- cleanup.

Prefer expand/migrate/contract for risky changes.

# API Planning

## Interface Template
### API/INT-XXX — [Operation]
- Consumer:
- Purpose:
- Requirement:
- Method/style:
- Auth:
- Authorization:
- Request:
- Validation:
- Response:
- Errors:
- Idempotency:
- Pagination:
- Rate limit:
- Side effects:
- Audit:
- Analytics:
- Compatibility:

Use existing API conventions when known.

## Errors
Plan meaningful errors for validation, unauthorized, forbidden, not found, conflict, rate limit, provider unavailable, and internal failure. Do not leak sensitive internals.

## Idempotency
Require it where clients, webhooks, or jobs may retry and duplicate side effects matter.

## Pagination
Use for potentially large collections. Match existing conventions.

## Versioning
Avoid premature version churn. Preserve public/external contracts carefully.

## Contracts
Use schema validation and generated/shared types where architecture supports it.

## Webhooks
Plan signature verification, replay protection where supported, idempotency, duplicate/out-of-order handling, queue processing, reconciliation, and failure visibility.

## API Test Coverage
Plan happy path, validation, auth, tenant access, idempotency, conflict, provider failure, edge cases, and contract regression.
