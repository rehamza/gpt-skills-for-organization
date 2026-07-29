---
name: engineering-handoff-readiness-check
description: Validates a Product Architect PRD or Engineering Handoff before detailed engineering planning. Use when requirements arrive and engineering needs to determine whether planning can proceed without inventing product decisions.
metadata:
  author: softquorra
  version: "1.0"
---

# Engineering Handoff Readiness Check

## Goal
Determine which parts of the approved handoff are ready for engineering planning and which are blocked.

## Workflow
1. Identify product, PRD/handoff version and approval status.
2. Verify P0 requirement IDs, P1/P2, non-goals, and critical acceptance criteria.
3. Check architecture/ADR status, data ownership/tenancy, integrations, AI, security/NFR, analytics, and release assumptions where relevant.
4. Identify conflicts between documents and separate blocking from non-blocking TBDs.
5. State planning areas that can proceed safely and return readiness classification.

## Output
- Inputs received
- Approved scope understood
- Missing information
- Conflicts
- Blocking decisions
- Non-blocking TBDs
- READY / READY WITH NON-BLOCKING TBDS / PARTIALLY READY / NOT READY

## Quality / Guardrails
- Do not resolve product ambiguity by inventing requirements.
- Preserve the latest clearly approved decision when traceable; otherwise escalate the conflict.
