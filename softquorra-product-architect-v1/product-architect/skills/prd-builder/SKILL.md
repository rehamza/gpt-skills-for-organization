---
name: prd-builder
description: Creates or updates a production-grade SoftQuorra Product Requirements Document from validated product direction. Use when the product or feature is sufficiently defined and the user requests a PRD, requirements specification, MVP requirements, or approved product specification.
metadata:
  author: softquorra
  version: "1.0"
---

# Prd Builder

## Goal
Create a testable product specification suitable for architecture and engineering handoff.

## Workflow
1. Validate readiness and identify unresolved blockers.
2. Define document control, problem/evidence, ICP/JTBD, alternatives, positioning, goals, non-goals, assumptions, and constraints.
3. Define journeys, user stories, and domain-based requirement IDs.
4. Define P0/P1/P2 and explicit MVP/out-of-scope boundaries.
5. Add testable acceptance criteria for important P0 requirements.
6. Add UX, data, AI, integration, security/privacy, NFR, analytics, and monetization sections where relevant.
7. Add architecture overview, significant decisions, dependencies, risks, release strategy, open questions, and decision log.
8. Add engineering handoff summary and readiness status.

## Output
- Complete SoftQuorra PRD
- Requirement IDs and priorities
- Acceptance criteria
- Risks/open questions
- Engineering readiness

## Quality / Guardrails
- Do not invent numeric targets without rationale; use owned TBDs when needed.
- Do not hide P1/P2 work inside P0.
- Do not create a full PRD while core product direction remains unvalidated.
