# SoftQuorra Engineering Planner Handoff Template

## Purpose
This is the contract between **SoftQuorra Product Architect** and **SoftQuorra Engineering Planner**.

The Architect defines approved product scope, requirements, architecture, constraints, and unresolved decisions.

The Engineering Planner converts this into implementation epics, stories, technical tasks, API/schema detail, sequencing, repository work, and coding prompts.

Do not hide unresolved product decisions inside engineering tasks.

---

# 1. Handoff Header

- Product:
- PRD version:
- Handoff version:
- Date:
- Product owner:
- Architect:
- Target release:
- Status:

# 2. Product Objective

One paragraph:
- customer;
- problem;
- outcome;
- why this release exists.

# 3. Primary ICP / Users

- Primary ICP:
- Buyer:
- End user:
- Key persona(s):
- Critical permissions/roles:

# 4. MVP Hypothesis

- We believe:
- For:
- Will result in:
- We will know when:

# 5. P0 Scope

List only approved MVP requirements.

| Requirement ID | Name | Outcome | Acceptance reference | Notes |
|---|---|---|---|---|

# 6. P1 / P2

List explicitly so engineering knows these are not P0.

## P1
- ...

## P2
- ...

# 7. Non-Goals / Out of Scope

- ...
- ...

Engineering must not quietly implement these without a scope decision.

# 8. Primary User Journeys

For each:
- actor;
- trigger;
- steps;
- value moment;
- errors/edge cases;
- success event.

# 9. Architecture Summary

- architecture style;
- frontend/web;
- mobile;
- backend;
- DB;
- cache;
- queue/jobs;
- storage;
- auth;
- billing;
- AI;
- integrations;
- hosting;
- observability.

Link/list approved ADRs.

# 10. C4 / System Diagram

Provide current System Context and Container diagram or reference to architecture doc.

# 11. Data Entities

| Entity | Purpose | Tenant/owner | Sensitive? | Key relationships |
|---|---|---|---|---|

Flag migration/import requirements.

# 12. API / Interface Domains

List major interfaces and who consumes them.

Do not specify every endpoint unless already a product/external contract.

# 13. Integrations

| ID | Provider | Purpose | Auth | Critical limits/failure behavior | Source/docs |
|---|---|---|---|---|---|

# 14. AI Components

For each:
- task ID;
- model/provider decision or TBD;
- input/context;
- output schema;
- tools;
- retrieval;
- approval/autonomy;
- eval;
- latency/cost constraints;
- fallback.

# 15. Security & Privacy Requirements

- authentication;
- authorization;
- tenant isolation;
- sensitive data;
- secrets;
- webhook verification;
- audit;
- retention/deletion;
- admin powers;
- compliance review items.

# 16. Non-Functional Requirements

List only actual targets/owned TBDs:
- performance;
- availability;
- scalability;
- reliability;
- accessibility;
- observability;
- backup/recovery;
- cost.

# 17. Analytics

List required events/metrics for MVP so engineering plans instrumentation as part of delivery.

# 18. Dependencies

## Internal
## External
## Data
## Vendor/Platform
## Client
## Legal/Security
## Design/Content

# 19. Architecture Decisions

| ADR | Decision | Status | Engineering implication |
|---|---|---|---|

# 20. Known Risks

| Risk | Impact | Mitigation | Engineering implication |
|---|---|---|---|

# 21. Open Decisions

For each:
- question;
- owner;
- deadline/decision point;
- what engineering work is blocked.

Do not mark READY if a critical blocking decision is unresolved.

# 22. Release Assumptions

- environments;
- rollout;
- migrations;
- feature flags;
- data migration;
- beta cohort;
- support/ops;
- rollback/failure plan.

# 23. Definition of Product Done

At product level:
- all P0 acceptance criteria met;
- required analytics present;
- security requirements addressed;
- critical AI eval thresholds met;
- billing/entitlements correct where applicable;
- critical integrations reliable;
- required documentation complete;
- release gate approved.

QA will later expand this into detailed verification/release checks.

# 24. Engineering Planner Instructions

Engineering Planner should:
1. preserve P0/P1/P2 boundary;
2. identify implementation dependencies;
3. create epics/stories/tasks;
4. define detailed schema/API contracts;
5. map tests to acceptance criteria;
6. identify technical spikes;
7. create incremental delivery sequence;
8. create Codex-ready prompts/tasks;
9. raise product/architecture conflicts instead of silently deciding;
10. reference requirement IDs and ADRs.

# 25. Final Status

Use exactly one:

**STATUS: READY FOR ENGINEERING PLANNER**

or

**STATUS: NOT READY FOR ENGINEERING PLANNER**

## Reasons / blockers
- ...
