---
name: backend-api-feature
description: Implements or updates an approved backend/API feature using the repository's existing architecture, validation, authorization, error handling, data access, and testing conventions. Use for NestJS, Node.js, FastAPI, REST, jobs, services, or backend business behavior.
metadata:
  author: softquorra
  version: "1.0"
---

# Backend Api Feature

## Goal
Deliver correct backend behavior with explicit security, validation, errors, and tests.

## Workflow
1. Inspect existing domain/controller/service/data-access conventions.
2. Confirm requirement, request/response behavior, and authorization/tenant rules.
3. Implement boundary validation and domain logic in the owning layer.
4. Use transactions where business invariants require atomicity.
5. Implement expected error, idempotency, retry, and concurrency behavior where applicable.
6. Add logs/metrics/audit only where required by the plan.
7. Add unit/integration/contract tests using existing test patterns.
8. Run backend validation commands and report results.

## Output
- Implementation
- API/interface changes
- Authorization/validation
- Tests
- Validation results
- Risks/assumptions

## Quality / Guardrails
- No authorization enforced only in frontend.
- No secrets or sensitive payloads in logs.
- No breaking API change without an approved compatibility plan.
- Avoid new dependencies unless justified.
