# SoftQuorra Product Requirements Document (PRD) Template

> Use this template after sufficient discovery. Remove sections that genuinely do not apply; do not fill sections with invented information.

# 1. Document Control

- Product:
- PRD ID:
- Version:
- Status: Discovery / Validation / Approved / Engineering / Released / Deprecated
- Product owner:
- Architect:
- Contributors:
- Created:
- Last updated:
- Research date:
- Target release:
- Related docs:

# 2. Executive Summary

- Product:
- Primary ICP:
- Buyer:
- Problem:
- Proposed solution:
- Core value proposition:
- Business model hypothesis:
- Platform:
- MVP objective:
- Recommendation:
- Confidence:

# 3. Product Vision

## Vision
What durable change should this product create?

## Why Now
What changed in technology, behavior, regulation, economics, or distribution?

## Why SoftQuorra
Why is SoftQuorra capable of winning/building this?

# 4. Problem Statement

## Problem
Describe the specific problem.

## Evidence
List evidence that it exists.

## Severity
How painful/costly is it?

## Frequency
How often does it occur?

## Current Workflow
How is it handled today?

## Cost of Problem
Time / money / revenue / risk / complexity / opportunity cost.

# 5. Target Market & ICP

- Market/category:
- Geography:
- Primary ICP:
- Secondary ICP:
- Buyer:
- End user:
- Decision maker:
- Company/user characteristics:
- Required trigger/behavior:
- Excluded segments for MVP:

# 6. Personas

For each material persona:

## Persona [name/role]
- Context:
- Goal:
- Current workflow:
- Pain:
- Motivation:
- Buying/usage trigger:
- Objections:
- Required permissions:
- Success outcome:

# 7. Jobs To Be Done

**When [situation], I want to [motivation/action], so I can [outcome].**

Include primary and secondary jobs.

# 8. Research Evidence

| ID | Claim | Evidence | Source | Date | Confidence | Product implication |
|---|---|---|---|---|---|---|

Label unsupported beliefs as assumptions.

# 9. Current Alternatives

Include direct competitors, adjacent products, manual workflows, agencies/internal staff, open source, generic AI, and doing nothing.

For each:
- use case;
- target audience;
- strengths;
- weaknesses;
- price/value metric;
- switching cost;
- implication.

# 10. Competitive Analysis

| Competitor | ICP | Core promise | Key capability | Pricing/value metric | Strength | Gap | Source/date |
|---|---|---|---|---|---|---|---|

## Differentiation Thesis
State why the target customer would switch/adopt. Do not rely on feature count alone.

# 11. Positioning

For **[target customer]**<br>
who **[problem]**,<br>
**[product]** is a **[category]**<br>
that **[primary benefit]**.<br>
Unlike **[alternative]**,<br>
it **[meaningful differentiator]**.

# 12. Goals

Use outcome-oriented goals.

- G-001:
- G-002:
- G-003:

For each include metric or verification approach.

# 13. Non-Goals

- NG-001:
- NG-002:
- NG-003:

Explicitly protect the release from adjacent scope.

# 14. Hypotheses

## HYP-001
- We believe:
- For:
- Will result in:
- Evidence today:
- Test:
- Success threshold:
- Failure threshold:
- Status:

# 15. Product Principles

Examples only:
- simple before powerful;
- human approval before risky automation;
- privacy by design;
- fast time-to-value;
- progressive disclosure.

Include only principles that constrain real decisions.

# 16. Assumptions

| ID | Assumption | Evidence | Impact if wrong | Validation method | Status |
|---|---|---|---|---|---|

# 17. Constraints

- Technical:
- Product:
- Time:
- Budget:
- Team:
- Platform:
- Data:
- Security:
- Compliance/legal:
- Contract/client:
- Operational:

# 18. Core User Journey

1. Trigger
2. Entry/acquisition
3. Signup/access
4. Onboarding/setup
5. First core action
6. Value moment
7. Repeat workflow
8. Collaboration/approval if relevant
9. Upgrade/retention

For each stage describe user goal, system behavior, failure/empty state, and measurement.

# 19. User Stories

## US-001
**As a** [persona]<br>
**I want** [capability]<br>
**so that** [outcome].

- Priority:
- Related requirement:
- Notes:

# 20. Functional Requirements

Use domain prefixes: AUTH, ORG, BILL, PROJ, AI, INT, etc.

## REQ-ID — Requirement Name

- Priority: P0 / P1 / P2
- User/persona:
- Description:
- Rationale:
- Preconditions:
- Trigger:
- Expected behavior:
- Inputs:
- Outputs:
- Business rules:
- Permissions:
- Edge cases:
- Failure behavior:
- Dependencies:
- Analytics events:
- Open questions:

### Acceptance Criteria
Use Given/When/Then or another testable form.

**Given**<br>
**When**<br>
**Then**

Do not invent numeric limits or performance thresholds without a basis. Mark them TBD with owner/validation method.

# 21. Feature Priority

## P0 — MVP
Required to prove/deliver the primary value hypothesis.

## P1 — Near-Term
Important after initial proof; not required for first launch.

## P2 — Future
Ideas intentionally excluded from initial commitment.

# 22. MVP Definition

- Core commercial/value hypothesis:
- Primary ICP:
- Primary user:
- Primary workflow:
- Activation event:
- Value moment:
- Required P0 features:
- Required integrations:
- Required operational process:
- Success metric:
- Failure metric:
- Validation period:
- Launch constraint:

# 23. Out of Scope

Explicitly list:
- features;
- user segments;
- platforms;
- integrations;
- automation;
- reporting;
- geographic support;
- enterprise requirements;
- future ideas not in this release.

# 24. UX Requirements

- Platforms:
- responsive behavior:
- accessibility expectation:
- navigation/information architecture:
- onboarding:
- loading/progress states:
- empty states:
- error/retry states:
- permissions/roles:
- confirmations/undo:
- notifications:
- localization:
- design system:
- risky-action UX:
- approval workflows:

# 25. Data Requirements

- Key entities:
- entity ownership:
- tenancy:
- relationships:
- source of truth:
- import/export:
- sensitive data:
- retention:
- deletion:
- auditability:
- backups:
- migration:
- data quality:
- analytics separation:

# 26. AI Requirements

Complete only if AI is material.

- AI use case:
- Why AI instead of deterministic logic:
- Model task:
- Inputs:
- Outputs:
- Context:
- Tools:
- Retrieval:
- Structured output/schema:
- Human approval:
- Autonomy level:
- Failure/fallback:
- Provider/model strategy:
- latency target/expectation:
- cost model:
- privacy/data handling:
- prompt/version management:
- abuse/safety considerations:

# 27. AI Evaluation

- Golden/evaluation dataset:
- Offline eval:
- Online monitoring:
- Human review:
- Task success:
- Accuracy/relevance:
- Groundedness:
- Hallucination/fabrication measure:
- Tool-call success:
- Structured-output validity:
- Latency:
- Cost per successful task:
- Escalation/approval rate:
- Release threshold:
- Regression threshold:

# 28. Integrations

## INT-001 — Provider / System
- Purpose:
- API/SDK:
- Authentication:
- Data sent:
- Data received:
- rate limits:
- webhook/events:
- retries:
- idempotency:
- timeout:
- failure UX:
- data/privacy implications:
- vendor dependency:
- current pricing/date:
- fallback/migration:

# 29. Security & Privacy

Use `11-security-and-privacy-standards.md`.

Document:
- identity/authentication;
- authorization;
- roles/permissions;
- tenant isolation;
- secrets;
- encryption;
- sensitive data;
- input validation;
- file handling;
- API protection;
- rate limiting;
- webhook verification;
- audit logging;
- payment boundary;
- retention/deletion;
- backup/recovery;
- incident needs;
- compliance considerations requiring specialist review.

# 30. Non-Functional Requirements

Only define relevant requirements.

## Performance
## Availability
## Scalability
## Reliability
## Security
## Privacy
## Accessibility
## Maintainability
## Observability
## Backup/Recovery
## Data Retention
## Internationalization
## Cost Efficiency

Each requirement should have a target or a clearly owned TBD.

# 31. Analytics & Instrumentation

## Event Taxonomy
For each:
- event name;
- trigger;
- actor;
- properties;
- privacy classification;
- business question answered.

Example events:
- account_created
- onboarding_completed
- project_created
- core_action_started
- core_action_completed
- recommendation_accepted
- subscription_started

# 32. Success Metrics

## North Star
- Metric:
- Why:

## Acquisition
## Activation
## Engagement
## Retention
## Revenue
## Quality
## Operational
## AI Quality (if relevant)

Avoid vanity metrics. Define formulas and windows where material.

# 33. Monetization

Use `06-monetization-framework.md`.

- Payer:
- business model:
- value metric:
- free/trial:
- plan structure:
- usage/entitlement boundaries:
- upgrade triggers:
- competitor benchmark:
- pricing hypothesis:
- variable cost:
- AI/API cost exposure:
- target margin hypothesis:
- enterprise/custom pricing needs:
- billing risks:

# 34. Technical Architecture

- Architecture style:
- web/frontend:
- mobile:
- backend:
- database:
- cache:
- queue/background jobs:
- storage:
- auth:
- authorization:
- realtime:
- AI/model layer:
- retrieval/search:
- billing:
- notifications:
- analytics:
- external services:
- hosting:
- observability:
- environments:
- CI/CD:
- deployment/rollback:
- backups:

Explain why.

# 35. Architecture Diagrams

Provide as useful:
- C4 System Context;
- C4 Container;
- deployment/data/sequence diagram for risky workflows.

Use Mermaid when appropriate.

# 36. Data Model Overview

For each key entity:
- purpose;
- owner/tenant;
- important fields conceptually;
- relationships;
- lifecycle;
- sensitive classification.

Do not turn the PRD into migration code.

# 37. API Domains

Identify major API surfaces only.

Example:
- `/auth`
- `/organizations`
- `/projects`
- `/billing`
- `/integrations`

Detailed endpoint contracts belong to engineering planning unless an external/public contract is itself a product requirement.

# 38. Architecture Decisions

List ADRs:
- ADR-001:
- ADR-002:

Use `10-architecture-decision-template.md`.

# 39. Build vs Buy

| Capability | Build/Buy | Candidate | Rationale | Cost | Risk | Exit path |
|---|---|---|---|---|---|---|

# 40. Dependencies

- internal;
- external vendor;
- platform;
- data;
- team/skill;
- contract/client;
- legal/compliance;
- launch.

# 41. Risk Register

| ID | Risk | Category | Likelihood | Impact | Evidence | Mitigation | Trigger/owner |
|---|---|---|---|---|---|---|---|

# 42. Release Strategy

## Phase 0 — Validation
## Phase 1 — MVP
## Phase 2 — Improve
## Phase 3 — Scale

Avoid speculative multi-year roadmaps.

# 43. Launch Readiness

- Product requirements reviewed
- P0 scope locked
- Architecture reviewed
- Security risks reviewed
- Analytics defined
- QA/acceptance criteria defined
- Critical integrations tested
- Billing tested where applicable
- Backup/recovery appropriate to risk
- Monitoring/alerts prepared
- Support/operations owner defined
- Rollback/failure plan defined
- Documentation/handoff complete

# 44. Open Questions

| ID | Question | Impact | Owner | Due/decision point |
|---|---|---|---|---|

# 45. Decision Log

| Date | Decision | Owner | Reason | Related ADR/requirement |
|---|---|---|---|---|

# 46. Engineering Handoff Summary

- Product objective:
- Primary ICP:
- MVP scope:
- P0 requirement IDs:
- architecture:
- key data entities:
- integrations:
- AI components:
- security/NFRs:
- dependencies:
- known risks:
- unresolved decisions:
- release assumptions:

# 47. Product Architect Recommendation

Choose:
- GO
- GO WITH CONDITIONS
- VALIDATE FIRST
- PIVOT
- DO NOT BUILD

Include:
- reasoning;
- strongest evidence;
- contradictory evidence;
- critical assumptions;
- next validation action.

# 48. Status

**READY FOR ENGINEERING PLANNER**

or

**NOT READY FOR ENGINEERING PLANNER — [reasons]**
