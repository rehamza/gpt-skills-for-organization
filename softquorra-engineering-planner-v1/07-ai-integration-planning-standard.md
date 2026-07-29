# SoftQuorra AI & Integration Engineering Planning Standard

# AI Implementation

For every AI task define:
- Task ID;
- Requirement;
- User/system trigger;
- Goal;
- Input;
- Context;
- Output;
- Schema;
- Failure tolerance.

## Implementation Components
Plan only required components:
- model client/provider adapter;
- prompt template/version;
- structured-output parser;
- retrieval;
- tool definitions;
- orchestration/state;
- approval step;
- persistence;
- queue/job;
- telemetry/evals.

## Model Choice
Use approved architecture if specified. If TBD, compare quality, latency, cost, tool/structured-output capability, context, privacy, availability, and provider constraints.

Use current official provider documentation for changing capabilities, pricing, and limits.

## Prompt Versioning
Plan stable prompt identifier/version, model/settings, output schema, eval baseline, deployment record, and rollback.

## Structured Output
Validate all model output consumed by code. Plan schema, invalid-output handling, retry/repair if justified, and telemetry.

## Retrieval
Only if approved/required. Plan source, permissions/tenancy, indexing/update, deletion, query, provenance/citations if required, and retrieval eval.

## Tool Calling / Agents
Each tool must have backend authorization, input schema, side-effect definition, idempotency, timeout, rate/spend limits, audit, and approval rule.

The model does not decide authorization.

## Evals
Plan automated/manual evals for task success, correctness, groundedness, schema validity, tool success, latency, cost, approval/edit/reject rate, and safety/abuse as applicable.

## Failure
Plan timeout, outage, rate limit, invalid response, hallucination, tool failure, partial completion, retry limit, fallback, and user-visible state.

# External Integration Planning

For each integration define:
- provider;
- approved use case;
- official API/SDK and version;
- authentication/scopes;
- sandbox/test environment;
- secret ownership/storage;
- limits/quotas;
- timeouts/retries;
- idempotency;
- webhooks;
- reconciliation;
- data sent/received;
- source of truth;
- failure UX;
- tests;
- observability.

Verify current provider constraints instead of guessing.
