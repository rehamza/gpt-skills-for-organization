# SoftQuorra Engineering Planning Framework

## Objective
Transform an approved product handoff into implementable, traceable engineering work without changing product intent.

# Phase 1 — Intake Validation
Capture product, PRD/handoff versions, P0/P1/P2, requirement IDs, acceptance criteria, architecture, ADRs, data entities, integrations, AI, security/NFRs, analytics, release assumptions, and open decisions.

Classify each input:
- Approved
- Proposed
- TBD
- Blocked
- Conflicting

Critical unresolved product decisions block implementation planning for affected work.

# Phase 2 — Requirement Traceability
Create a map:

| Requirement | User outcome | Domain | Epic | Data/API/UI/AI | Tests | Status |
|---|---|---|---|---|---|---|

Every P0 requirement must map to implementation and verification.

Identify duplicates, conflicts, missing acceptance criteria, cross-cutting dependencies, and hidden operational requirements.

# Phase 3 — Existing System / Repository Discovery
For existing projects inspect available repo tree, workspace config, architecture docs, schema/migrations, API modules, frontend routes/components, jobs/queues, integrations, tests, CI/CD, and environment configuration examples.

Output:
- current architecture;
- reusable modules;
- change surfaces;
- technical debt affecting P0;
- migration constraints.

Do not invent file paths when not provided.

# Phase 4 — Domain Decomposition
Identify implementation domains such as Identity/Auth, Organizations/Tenancy, Billing, Core Domain, AI, Integrations, Notifications, Analytics, and Administration.

Map ownership and boundaries.

# Phase 5 — Technical Design
For each P0 capability decide implementation-level details:
- domain/module;
- data changes;
- APIs/interfaces;
- frontend/mobile;
- background work;
- integrations;
- permissions;
- AI workflow;
- analytics;
- errors/failure;
- tests;
- observability;
- rollout.

Raise ADRs only when architecturally significant.

# Phase 6 — Epics
Each epic should produce a coherent capability, map to requirement IDs, have a measurable completion condition, expose dependencies, and be decomposable into stories/tasks.

Prefer capability-oriented epics over generic “Backend” or “Frontend” epics.

# Phase 7 — Stories / Tasks
Use `05-task-story-standard.md`.

Separate technical spikes, production implementation, migrations/backfills, test automation, observability, and rollout work.

# Phase 8 — Dependency Graph
Identify hard prerequisites, soft prerequisites, external lead time, product decisions, shared schema/API, credentials, migrations, design assets, and provider approvals.

Find the critical path and parallelizable work.

# Phase 9 — Delivery Slices
Prefer end-to-end slices that produce testable behavior.

Example:
1. auth/tenant foundation;
2. create/import core object;
3. validate/process core object;
4. show result;
5. AI workflow;
6. billing/limits;
7. production hardening.

# Phase 10 — Codex Packaging
Group tasks into bounded work packages small enough to understand, implement, test, and review independently.

Use `09-codex-work-package-template.md`.

# Phase 11 — Engineering Review
Check that all P0 is traceable; P1/P2 remains excluded; migrations are safe; APIs/data are consistent; permissions explicit; failure behavior planned; analytics included; AI evals included; tests mapped; observability included; deploy/rollback considered; blockers visible.

# Phase 12 — QA Handoff
Provide QA with requirement/acceptance mapping, implemented slices, risk areas, integration failure cases, migration behavior, AI eval expectations, feature flags, known limitations, and release assumptions.

Final QA/release approval belongs to QA & Release Manager.
