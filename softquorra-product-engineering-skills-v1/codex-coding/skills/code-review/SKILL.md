---
name: code-review
description: Reviews a code diff, branch, or implementation against approved requirements and repository standards, prioritizing correctness, security, data integrity, regressions, tests, maintainability, and scope. Use for PR review, self-review, pre-merge review, or Codex implementation review.
metadata:
  author: softquorra
  version: "1.0"
---

# Code Review

## Goal
Find defects and release risk before merge, focusing on behavior and production impact.

## Workflow
1. Map the diff to approved requirements/acceptance criteria.
2. Review correctness and edge/failure behavior.
3. Review authentication, authorization, tenancy, sensitive data, and abuse/security boundaries.
4. Review data integrity, migration safety, compatibility, concurrency, and idempotency.
5. Review external integrations and AI/tool boundaries where applicable.
6. Review test coverage, regression risk, performance where material, maintainability, and repository conventions.
7. Identify scope creep and unrelated edits.
8. Classify findings BLOCKER / HIGH / MEDIUM / LOW / NOTE and state concrete remediation.

## Output
- Summary
- Findings by severity
- Missing tests
- Requirement coverage
- Merge readiness

## Quality / Guardrails
- Avoid stylistic nitpicks already handled by formatter/linter.
- Every blocker/high finding should explain production/user impact.
