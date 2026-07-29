---
name: architecture-decision-draft
description: Creates a product-level Architecture Decision Record for a significant technical decision after requirements are understood. Use for stack, database, architecture style, auth, AI provider strategy, build-vs-buy, service boundaries, or material technical tradeoffs.
metadata:
  author: softquorra
  version: "1.0"
---

# Architecture Decision Draft

## Goal
Document why a significant architecture choice is appropriate for this product.

## Workflow
1. Define context, verified requirements, assumptions, and ranked decision drivers.
2. Compare 2–4 credible options across delivery speed, complexity, reliability, performance, security, cost, team fit, lock-in, and migration.
3. Recommend the simplest option satisfying actual requirements.
4. Record benefits, drawbacks, accepted tradeoffs, consequences, and rollout/migration.
5. Define conditions that should trigger revisiting the decision.

## Output
- ADR title/status/date
- Context
- Decision drivers
- Options
- Decision/rationale
- Consequences
- Cost/security
- Migration
- Revisit conditions
- References

## Quality / Guardrails
- Preferred technology does not mean mandatory technology.
- Do not choose technology because it is fashionable or theoretically more scalable.
