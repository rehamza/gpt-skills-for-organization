---
name: codex-work-package-builder
description: Creates a bounded repository-aware Codex coding work package from an approved engineering task or story. Use for Codex prompts, VS Code implementation packages, coding tasks, implementation briefs, or handoff to Codex.
metadata:
  author: softquorra
  version: "1.0"
---

# Codex Work Package Builder

## Goal
Turn one approved engineering unit into a coding package that Codex can implement and verify independently.

## Workflow
1. Define one bounded objective and trace it to requirement/story/ADR IDs.
2. State prerequisites and dependency packages.
3. Separate confirmed repository files/modules from paths Codex must discover.
4. Define required behavioral changes and applicable data/API/UI/AI/security/telemetry work.
5. Define tests, acceptance criteria, non-goals, and validation commands only when known.
6. Require a completion report and define stop conditions for scope, architecture, migration, secret/provider, or safety conflicts.

## Output
- CODEX-XXX title/objective
- Product/engineering trace
- Prerequisites
- Known vs discover repository context
- Required changes
- Tests
- Acceptance criteria
- Non-goals
- Validation
- Completion evidence
- Stop conditions

## Quality / Guardrails
- Always tell Codex to inspect the repository and follow existing architecture/conventions before editing.
- Do not ask Codex to build an entire product in one work package.
