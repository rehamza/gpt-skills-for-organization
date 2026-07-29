---
name: engineering-handoff-builder
description: Builds the final Product Architect to Engineering Planner handoff from an approved PRD and architecture. Use when product scope is approved and the user wants to hand the product or feature to engineering planning.
metadata:
  author: softquorra
  version: "1.0"
---

# Engineering Handoff Builder

## Goal
Create a stable contract that lets Engineering Planner work without reinventing product decisions.

## Workflow
1. Confirm PRD status/version and summarize objective, ICP, buyer/user, and MVP hypothesis.
2. List every approved P0 requirement ID and preserve P1/P2/non-goals.
3. Summarize journeys, architecture, ADRs, data entities/tenancy, integrations, and AI tasks.
4. Summarize security/NFR, analytics, dependencies, known risks, and release assumptions.
5. List unresolved decisions, owner, impact, and what they block.
6. Determine whether engineering planning can proceed.

## Output
- Handoff header
- Product objective/ICP
- MVP/P0
- P1/P2/non-goals
- Journeys
- Architecture/ADRs
- Data/integrations/AI
- Security/NFR/analytics
- Dependencies/risks/open decisions
- Release assumptions
- Status

## Quality / Guardrails
- End with STATUS: READY FOR ENGINEERING PLANNER or STATUS: NOT READY FOR ENGINEERING PLANNER — [reasons].
- Do not hide unresolved product decisions in technical notes.
