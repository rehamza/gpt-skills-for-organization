---
name: release-readiness-gate
description: Produces an evidence-based GO, CONDITIONAL GO, or NO-GO release decision from requirement verification, defects, migrations, integrations, AI quality, security, observability, rollout, rollback, and accepted risks. Use at the final release gate.
metadata: {author: softquorra, version: "1.0"}
---
# Release Readiness Gate
Review P0 coverage, open defects, security, data/migration, integrations, AI, observability, deployment, rollback, flags/cohorts, support ownership, known limitations, and accepted risks.
Return GO / CONDITIONAL GO / NO-GO.
List blockers, conditions, owner, monitoring, rollback trigger, and evidence.
Critical unresolved blockers mean NO-GO.
