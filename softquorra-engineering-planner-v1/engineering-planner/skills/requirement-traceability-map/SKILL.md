---
name: requirement-traceability-map
description: Maps approved PRD requirements to engineering domains, epics, tasks, interfaces, tests, and status. Use when planning, auditing coverage, finding orphan requirements, or verifying every P0 requirement has implementation and verification coverage.
metadata:
  author: softquorra
  version: "1.0"
---

# Requirement Traceability Map

## Goal
Make every material engineering activity traceable to approved product or technical intent.

## Workflow
1. Extract all P0 requirements and critical acceptance criteria.
2. Map each to user/system outcome and engineering domain.
3. Map each to epics, stories/tasks, data/API/UI/AI/integration impact, and test/eval coverage.
4. Identify dependencies and blockers.
5. Identify P0 requirements missing implementation or verification and tasks without requirement/technical justification.

## Output
- Traceability table: Requirement | Outcome | Domain | Epic | Tasks | Interfaces | Verification | Status
- Missing coverage
- Duplicate/conflicting work
- Scope drift
- Blockers

## Quality / Guardrails
- Do not mark a requirement covered merely because a similarly named task exists.
- Preserve requirement IDs exactly.
