# SoftQuorra Epic, Story & Engineering Task Standard

## IDs
Suggested:
- EPIC-001
- STORY-001
- TASK-001
- SPIKE-001
- MIG-001
- TEST-001
- OBS-001

Preserve project issue IDs when an existing tracker convention exists.

# Epic Template
## EPIC-XXX — [Outcome/Capability]

### Goal
What coherent capability becomes available?

### Requirement References
- REQ-...
- US-...
- ADR-...

### Scope
Included:
- ...

Excluded:
- ...

### Dependencies
- ...

### Deliverable
Observable product/system result.

### Epic Acceptance
- ...

### Risks
- ...

### Stories / Work Packages
- STORY-...
- ...

# Story Template
## STORY-XXX — [Title]

### Product Trace
- Requirement:
- User story:
- ADR:
- Epic:

### Objective
What behavior/outcome is implemented?

### Existing Context
Known modules/interfaces. Do not invent paths.

### Functional Behavior
- ...

### Technical Notes
- ...

### Data Changes
- none / describe

### API / Interface Changes
- none / describe

### UI / Mobile Changes
- none / describe

### AI / Integration Changes
- none / describe

### Security / Permission
- ...

### Analytics / Observability
- ...

### Dependencies
- ...

### Acceptance Criteria
Given / When / Then.

### Test Requirements
- unit:
- integration:
- E2E:
- special:

### Definition of Done
- behavior works;
- tests pass;
- migration safe if applicable;
- telemetry included if required;
- docs/contracts updated;
- acceptance criteria demonstrated.

# Technical Task Template
## TASK-XXX — [Technical objective]

- Parent Epic/Story:
- Requirement references:
- Type: Backend / Frontend / Mobile / Data / AI / Integration / DevOps / Security / Test / Observability
- Objective:
- Preconditions:
- Known files/modules:
- Candidate/TBD files if repo unknown:
- Implementation:
- Constraints:
- Error/failure behavior:
- Tests:
- Validation:
- Dependencies:
- Estimate/size:
- Done when:

# Spike Template
## SPIKE-XXX — [Unknown to resolve]

- Decision blocked:
- Question:
- Why unknown:
- Method/prototype:
- Time/effort bound:
- Evidence required:
- Output:
- ADR/product decision required?
- Exit criteria:

A spike is not production implementation.

# Quality Rules
Good work items are bounded, traceable, independently reviewable, dependency-aware, testable, and have completion evidence.

Bad: `Implement backend.`

Better: `Implement schema-validated deck import endpoint with validation result persisted and integration tests mapped to DECK-001.`

# Scope Change Rule
If a task requires unapproved product behavior, label:

**CHANGE REQUEST — Product Architect/Product Owner approval required**

Describe current requirement, discovered issue, proposed change, engineering impact, and alternatives. Do not put the change into committed scope until approved.
