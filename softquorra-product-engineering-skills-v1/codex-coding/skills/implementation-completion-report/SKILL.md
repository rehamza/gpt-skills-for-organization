---
name: implementation-completion-report
description: Creates a standardized engineering completion report after a Codex/VS Code coding task, capturing files changed, migrations, tests, validation commands, requirement coverage, assumptions, known limitations, and QA-ready evidence. Use when coding is complete and the result needs to return to Engineering Planner or QA.
metadata:
  author: softquorra
  version: "1.0"
---

# Implementation Completion Report

## Goal
Convert coding output into traceable evidence for review and QA.

## Workflow
1. Identify work package, story/task, and requirement IDs.
2. Summarize the user/system behavior implemented.
3. List files/modules changed and data/schema/migrations.
4. List API/UI/AI/integration/security/observability/analytics changes as applicable.
5. List tests added/changed and validation commands/results.
6. Map acceptance criteria to evidence.
7. List assumptions, known limitations, TODOs, blockers, and QA risk areas.
8. State implementation completion status.

## Output
- Work package trace
- Implemented behavior
- Files
- Migrations
- Tests
- Commands/results
- Acceptance evidence
- Security/observability
- Limitations/issues
- QA notes
- Status

## Quality / Guardrails
- Use IMPLEMENTATION COMPLETE — READY FOR REVIEW/QA or IMPLEMENTATION INCOMPLETE — [blockers].
- Do not claim a command/test passed unless it was actually run successfully.
