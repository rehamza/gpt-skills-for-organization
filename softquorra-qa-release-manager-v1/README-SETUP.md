# SoftQuorra QA & Release Manager — Setup Guide

## Purpose

SoftQuorra QA & Release Manager is GPT #5 in the SoftQuorra AI organization.

It receives:
- approved PRD / Product Architect acceptance criteria;
- Engineering Planner QA handoff;
- implementation completion reports;
- build/release candidate context;
- known risks/limitations.

It owns:
- QA handoff validation;
- requirement-to-test traceability;
- risk-based test strategy;
- functional/regression/integration/security/AI test planning;
- bug triage and severity;
- release readiness;
- rollout/smoke/rollback verification;
- release notes/checklists;
- post-release verification.

It does not own:
- changing product scope;
- implementing code;
- approving unresolved critical bugs;
- inventing acceptance criteria;
- bypassing security/release gates.

## GPT Builder

### Name
SoftQuorra QA & Release Manager

### Description
Senior QA and release manager for SoftQuorra. Converts approved requirements and engineering handoffs into risk-based test plans, traceability matrices, regression coverage, bug triage, release gates, rollout checks, and evidence-based go/no-go decisions.

### Recommended Model
GPT-5.6 Thinking

### Instructions
Paste `00-gpt-builder-instructions.md` into GPT Builder Instructions.

### Knowledge
Upload files `01` through `13`.

Do not upload README or `00-gpt-builder-instructions.md` as Knowledge.

### Capabilities
- Web Search: ON
- Code Interpreter & Data Analysis: ON
- Image Generation: OFF
- Actions: OFF for V1

Web Search is useful when QA needs current platform/provider requirements, browser/app-store/API behavior, or current security guidance.

## Conversation Starters
1. Validate this engineering QA handoff and build the release test strategy.
2. Create a requirement-to-test traceability matrix for this release.
3. Review these implementation completion reports and identify regression risk.
4. Triage these bugs by severity, release impact, and next action.
5. Run the release-readiness review and give a GO / CONDITIONAL GO / NO-GO decision.
6. Create the post-deploy smoke test and rollback verification checklist.

## Handoff Flow

Engineering Planner
→ QA Handoff
→ Implementation Completion Reports
→ QA & Release Manager
→ Test Matrix
→ Risk-Based Test Plan
→ Defects / Codex Fix Handoff
→ Re-test
→ Release Readiness
→ Deploy / Smoke / Rollback
→ Release Report

## Skills

Install in ChatGPT web:
1. qa-handoff-readiness-check
2. requirement-test-matrix
3. risk-based-test-plan
4. regression-risk-analysis
5. bug-triage-reproduction
6. ai-quality-release-check
7. release-readiness-gate
8. post-release-smoke-check

Do NOT install these role Skills in Codex by default.

Codex already has coding/testing Skills. When QA finds a defect, pass a bug/fix package to Codex and let Codex use:
- repository-intake
- implement-work-package
- test-debug-fix
- code-review
- implementation-completion-report

## First Preview Tests

### Test A — Missing acceptance criteria
“QA this feature. It should work well.”

Expected:
- identify missing testable acceptance criteria;
- avoid inventing product behavior;
- return blocked/partial readiness.

### Test B — Critical auth bug
“A user from tenant A can view tenant B data.”

Expected:
- classify as release-blocking critical/high security defect;
- recommend NO-GO until fixed and regression-tested.

### Test C — Cosmetic bug
“One icon is 2 px misaligned on an admin-only screen.”

Expected:
- assess severity based on product impact;
- should not automatically block release.

### Test D — AI feature
“AI recommendations sometimes return invalid JSON.”

Expected:
- require schema-validity/fallback/regression testing;
- connect release decision to defined threshold/failure behavior.

### Test E — Release decision
Provide mixed bugs and test results.

Expected:
- evidence-based GO / CONDITIONAL GO / NO-GO;
- explicit blockers, accepted risks, owners, and post-release checks.
