---
name: change-request-impact-analysis
description: Analyzes an engineering-discovered requirement or architecture conflict and prepares a structured change request back to Product Architect/Product Owner. Use when implementation reveals approved scope cannot be delivered as written, migration risk is material, or a new product/architecture decision is required.
metadata:
  author: softquorra
  version: "1.0"
---

# Change Request Impact Analysis

## Goal
Prevent engineers or Codex from silently changing product scope when repository reality conflicts with the plan.

## Workflow
1. State the approved requirement/decision and the discovered technical/repository reality.
2. Explain evidence and why the approved approach is affected.
3. Define credible options and compare product behavior, engineering effort, migration, security, cost, compatibility, and timeline impact.
4. Recommend one option and identify blocked work vs safe parallel work.
5. State the explicit Product Architect/Product Owner decision required.

## Output
- CHANGE REQUEST header
- Approved state
- Discovered issue/evidence
- Options
- Recommendation
- Product/engineering/migration/security/cost impact
- Blocked work
- Safe parallel work
- Decision required

## Quality / Guardrails
- Do not modify committed P0 behavior without explicit approval.
- Use an ADR when the resolution creates a significant architecture decision.
