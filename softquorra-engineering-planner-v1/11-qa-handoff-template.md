# Engineering Planner → QA & Release Manager Handoff Template

## Purpose
Provide GPT #5 with traceable implementation intent and high-risk verification areas without duplicating the full engineering backlog.

# Header
- Product:
- PRD version:
- Engineering plan version:
- Release/build:
- Date:

# P0 Traceability
| Requirement | Implementation epic/package | Acceptance criteria | Test coverage planned |
|---|---|---|---|

# Critical User Journeys
- ...

# Risk Areas
Consider as applicable:
- auth/authz;
- tenancy;
- billing;
- migrations;
- external integrations;
- AI behavior;
- concurrency/idempotency;
- permissions;
- data deletion/export;
- platform-specific behavior.

# Data / Migration
- schema changes:
- backfill:
- rollback:
- compatibility:
- validation:

# Integrations
For each critical provider test success, timeout, rate limit, invalid credential, webhook duplicates/out-of-order events, provider outage, and reconciliation as applicable.

# AI
For each AI task:
- task;
- release eval;
- expected quality threshold;
- invalid output;
- fallback;
- tool/approval behavior;
- cost/latency signal;
- known limitations.

# Security
- roles/permissions;
- tenant boundaries;
- sensitive operations;
- abuse/rate limiting;
- admin capabilities;
- webhook/payment security.

# Observability
- required logs;
- metrics;
- alerts;
- analytics events;
- audit events.

# Feature Flags / Rollout
- flags:
- default state:
- cohort:
- rollback:
- cleanup condition:

# Known Limitations
- ...

# Open Bugs / Accepted Risks
- ...

# QA Blockers
- ...

# Planner Status
**READY FOR QA PLANNING**

or

**NOT READY FOR QA PLANNING — [reasons]**
