# SoftQuorra Architecture Decision Record (ADR) Template

Use ADRs for decisions that materially affect architecture, cost, security, scalability, developer workflow, vendor dependency, or future migration.

Do not create ADRs for trivial code-level preferences.

---

# ADR-[NNN]: [Decision Title]

- **Status:** Proposed / Accepted / Superseded / Deprecated
- **Date:**
- **Owners:**
- **Product/Project:**
- **Related PRD requirements:**
- **Supersedes:**
- **Superseded by:**

## Context
What problem/constraint requires a decision?

Include:
- relevant product requirements;
- scale/load assumptions;
- team/operational constraints;
- security/privacy;
- cost;
- deadline;
- existing architecture.

Clearly mark assumptions.

## Decision Drivers
Rank the factors that matter.

Examples:
- delivery speed;
- reliability;
- performance;
- team expertise;
- data consistency;
- ecosystem;
- platform compatibility;
- cost;
- lock-in;
- compliance.

## Options Considered

### Option A — [name]
Description.

**Benefits**
- ...

**Costs/Tradeoffs**
- ...

**Risks**
- ...

### Option B — [name]
...

### Option C — [name]
...

## Decision
State the selected option in one direct paragraph.

## Why This Option
Explain how it best satisfies the decision drivers.

Do not say “best practice” without connecting it to this product.

## Consequences

### Positive
- ...

### Negative
- ...

### Accepted Tradeoffs
- ...

## Cost Implications
- implementation cost:
- infrastructure/vendor cost:
- operational burden:
- expected migration cost:

Label estimates.

## Security / Privacy Implications
- ...

## Migration / Rollout
- steps:
- compatibility:
- rollback:
- data migration:
- operational change:

## Observability / Success Criteria
How will we know the decision works?

## Revisit When
Examples:
- tenant count exceeds X;
- workload profile changes;
- provider pricing changes;
- SLA changes;
- new compliance requirement;
- team ownership splits.

Do not invent numeric triggers; define them from product requirements.

## References
- official documentation;
- benchmarks;
- PRD;
- spike results;
- related ADRs.
