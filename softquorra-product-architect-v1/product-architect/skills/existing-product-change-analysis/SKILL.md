---
name: existing-product-change-analysis
description: Analyzes a feature or requirement change for an existing product such as Socialope. Use when adding, removing, redesigning, automating, integrating, or changing behavior in a product that already exists.
metadata:
  author: softquorra
  version: "1.0"
---

# Existing Product Change Analysis

## Goal
Define the smallest justified product change while protecting existing behavior and users.

## Workflow
1. Establish current behavior from supplied/internal/verified context.
2. State proposed behavior and the user problem/evidence.
3. Classify the change: bug, UX improvement, capability, integration, autonomy change, monetization change, or architecture-impacting requirement.
4. Map affected journeys, roles, data, APIs, integrations, AI, billing, security, analytics, and operations.
5. Identify compatibility, migration, platform/API, and rollout implications.
6. Challenge whether a smaller change solves the same problem.
7. Define P0/P1/P2, non-goals, acceptance conditions, success metrics, risks, and open decisions.
8. State whether an ADR, further validation, or engineering handoff is required.

## Output
- Existing behavior
- Proposed behavior
- Problem/evidence
- Impact map
- Scope/priority
- Migration/compatibility
- Metrics
- Risks/open questions
- Recommendation
- Handoff readiness

## Quality / Guardrails
- Never present assumptions about current product behavior as facts.
- For Socialope, verify implementation or current platform/API behavior when material.
