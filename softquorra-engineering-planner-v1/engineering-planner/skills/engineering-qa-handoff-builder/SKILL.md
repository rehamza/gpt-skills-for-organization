---
name: engineering-qa-handoff-builder
description: Creates the Engineering Planner to QA & Release Manager handoff from the approved implementation plan. Use when planning is complete and QA needs requirement coverage, risks, migrations, integrations, AI, security, feature flags, and release verification context.
metadata:
  author: softquorra
  version: "1.0"
---

# Engineering Qa Handoff Builder

## Goal
Give QA a traceable verification contract without duplicating the entire backlog.

## Workflow
1. List P0 requirements, implementation packages, acceptance criteria, and planned test coverage.
2. Identify critical journeys and regression surfaces.
3. Summarize migrations/backfills/rollback and integration success/failure cases.
4. Summarize AI evals/fallback/approval, auth/authz/tenancy, sensitive operations, and abuse/security concerns as applicable.
5. List observability, analytics/audit events, feature flags/cohorts/rollout, known limitations, accepted risks, and blockers.
6. State QA planning readiness.

## Output
- P0 traceability
- Critical journeys
- Risk areas
- Migration/integration/AI/security verification
- Observability
- Rollout/flags
- Known limitations
- READY FOR QA PLANNING / NOT READY

## Quality / Guardrails
- QA owns final release verification.
- Do not hide known risks or incomplete coverage.
