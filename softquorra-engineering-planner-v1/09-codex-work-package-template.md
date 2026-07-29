# SoftQuorra Codex Work Package Template

## Purpose
Create bounded coding instructions that can be implemented and reviewed independently.

Do not generate one giant “build the product” prompt.

# CODEX-[NNN] — [Work Package Title]

## Objective
Implement [specific behavior/outcome].

## Product Trace
- Epic:
- Story/task:
- Requirement IDs:
- ADRs:

## Prerequisites
- prior packages/tasks;
- migrations;
- credentials;
- approved decisions;
- repository branch/state.

## Repository Context

### Known
List only files/modules confirmed from repository context.

### Candidate / To Discover
When exact paths are unknown, list logical module/search target and conventions to follow.

Instruction to Codex:
> Inspect the repository before editing. Follow existing architecture, naming, validation, test, and error-handling conventions. Do not create parallel abstractions when an existing module already owns this behavior.

## Required Changes
1. ...
2. ...
3. ...

Be behavioral and technically specific without forcing unsupported implementation details.

## Data Changes
- schema:
- constraints:
- indexes:
- migration:
- backfill:
- rollback/compatibility:

## API / Interface Changes
- operation:
- auth/authz:
- validation:
- response/error:
- idempotency:
- compatibility:

## UI / Mobile Changes
- routes/screens:
- components:
- state/query:
- loading/error/empty:
- accessibility:
- analytics:

## AI / Integration Changes
- model/tool/provider:
- schema:
- prompt/eval:
- retry/fallback:
- approval:
- telemetry:

## Security Requirements
- ...

## Observability
- logs:
- metrics:
- errors:
- audit:
- product analytics:

## Tests Required
- unit:
- integration:
- component:
- E2E:
- migration:
- AI eval:
- failure case:

## Acceptance Criteria
Given / When / Then.

## Non-Goals
Explicitly state what this work package must not implement.

## Validation Commands
Only include commands confirmed from repo context.

If unknown:
> Discover and use the repository's existing lint, typecheck, test, and build commands.

## Completion Evidence
Codex/engineer should report:
- files changed;
- migrations created;
- tests added/updated;
- commands run/results;
- acceptance criteria satisfied;
- assumptions;
- unresolved issues.

## Stop Conditions
Stop and raise a blocker if:
- requirement conflicts with repo reality;
- migration risks data loss without approval;
- required secret/provider capability is absent;
- task requires an unapproved product/architecture change;
- tests reveal unrelated critical breakage needing scope decision.
