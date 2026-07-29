# Product Architect → Engineering Planner Input Contract

## Goal
Ensure Engineering Planner receives enough approved information to plan implementation without recreating product discovery.

Preferred source artifact:
**SoftQuorra Engineering Handoff**

# Required for Full Planning

## Product
- name;
- objective;
- primary ICP/user;
- release/MVP goal.

## Scope
- P0 requirements;
- requirement IDs;
- P1/P2;
- explicit non-goals.

## Behavior
- primary journeys;
- acceptance criteria;
- key business rules;
- error/failure expectations where material.

## Architecture
- architecture style;
- major system components;
- approved technology choices;
- relevant ADRs;
- external services.

## Data
- principal entities;
- ownership/tenancy;
- sensitive data;
- import/migration requirements.

## Integrations
- provider/purpose;
- critical constraints;
- auth/scopes where known.

## AI
- task;
- autonomy/approval;
- required eval;
- privacy/cost constraints.

## Security/NFR
- authentication;
- authorization;
- tenancy;
- sensitive data;
- performance/availability expectations;
- accessibility;
- observability;
- backup/recovery where material.

## Analytics
- required product events;
- success metrics requiring instrumentation.

## Release
- rollout assumptions;
- target platform;
- feature flags/cohort if required;
- migration constraints.

## Open Decisions
- unresolved questions;
- owner;
- what they block.

# Readiness Classification

## READY
P0 scope and critical architecture/product decisions are sufficiently clear for detailed planning.

## READY WITH NON-BLOCKING TBDS
Planning can proceed with explicit TBD tasks/owners that do not alter core design.

## PARTIALLY READY
Some domains can be planned; blocked domains remain uncommitted.

## NOT READY
The planner would need to invent product behavior, critical security/architecture, or acceptance expectations.

# Conflict Resolution
If PRD and Engineering Handoff differ:
1. identify version/date/status;
2. use the latest explicitly approved source when unambiguous;
3. record the discrepancy;
4. request Product Architect/Product Owner resolution when ambiguous.

Do not silently merge conflicting requirements.

# Same-Conversation Handoff
When Product Architect and Engineering Planner are used in the same ChatGPT conversation, the planner should first summarize:

**Input understood**
- PRD version/status:
- P0:
- architecture:
- ADRs:
- blockers:

Then ask only for information that is actually missing.

Do not force the user to re-paste information already present in the current conversation.

# New-Conversation Handoff
Preferred attachment bundle:
1. `engineering-handoff.md`
2. `prd.md`
3. `architecture.md` if needed
4. relevant ADRs
5. repo tree/context for existing-system work

The handoff should contain enough context that the planner can work when the full research conversation is unavailable.
