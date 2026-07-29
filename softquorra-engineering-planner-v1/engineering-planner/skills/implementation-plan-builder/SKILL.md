---
name: implementation-plan-builder
description: Converts an approved PRD/handoff and available repository context into a complete SoftQuorra implementation plan. Use for engineering planning, technical planning, delivery design, implementation sequencing, or implementation-plan.md.
metadata:
  author: softquorra
  version: "1.0"
---

# Implementation Plan Builder

## Goal
Turn approved scope into an implementation-ready plan without changing product intent.

## Workflow
1. Run readiness validation.
2. Inspect available repository/system context and distinguish existing vs new surfaces.
3. Build P0 traceability and domain/module map.
4. Plan data/schema/migrations, APIs/interfaces, frontend/mobile, AI/integrations, security/NFR, analytics, and observability as applicable.
5. Define epics, stories/tasks, spikes, tests/evals, and dependencies.
6. Build dependency graph, vertical delivery slices, migration/rollout/rollback, and effort ranges when requested.
7. Define Codex work packages and QA handoff inputs.
8. Return implementation readiness status.

## Output
- Input validation
- P0 traceability
- Repo assessment
- Implementation architecture
- Data/API/UI/AI/integration plans
- Epic/task backlog
- Dependencies and delivery slices
- Test/observability plan
- Rollout
- Codex packages
- QA inputs
- READY/NOT READY status

## Quality / Guardrails
- Never invent exact repository paths when context is absent; mark them candidate/TBD.
- Do not promote P1/P2 into P0.
- Use preferred technology as a default, not a mandate.
