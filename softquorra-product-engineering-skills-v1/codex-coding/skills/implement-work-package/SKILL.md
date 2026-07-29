---
name: implement-work-package
description: Implements a bounded approved Codex/engineering work package in the current repository, including code, tests, migrations where approved, validation commands, and a completion report. Use as the default coding skill when a CODEX work package or engineering task is provided.
metadata:
  author: softquorra
  version: "1.0"
---

# Implement Work Package

## Goal
Implement the approved behavior completely while preserving scope and repository conventions.

## Workflow
1. Read the entire work package, traceability IDs, acceptance criteria, prerequisites, and non-goals.
2. Run repository intake for the affected area and verify the package matches repo reality.
3. Stop and report if work requires unapproved product behavior, a destructive migration without plan, a major new architecture decision, or unavailable required provider/secret.
4. Implement the smallest complete change and reuse existing modules/patterns.
5. Add or update tests, migrations, telemetry, and docs required by the package.
6. Run relevant lint, typecheck, tests, build, and migration checks discovered from the repo.
7. Fix failures caused by the change and review the final diff for scope creep.
8. Produce a structured completion report with evidence.

## Output
- Work package/requirement IDs
- Files changed
- Behavior implemented
- Schema/migrations
- Tests
- Commands/results
- Acceptance criteria status
- Assumptions
- Remaining issues

## Quality / Guardrails
- Do not perform unrelated refactors.
- Do not weaken valid tests to make the suite pass.
- Do not silently change product scope.
