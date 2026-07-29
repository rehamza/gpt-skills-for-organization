---
name: post-release-smoke-check
description: Creates or evaluates a focused post-deployment smoke verification for a release, covering health, auth, critical P0 journeys, data, integrations, billing, AI, permissions, monitoring, migration status, and rollback signals. Use immediately after deployment or during rollout.
metadata: {author: softquorra, version: "1.0"}
---
# Post-Release Smoke Check
Confirm build/version and deployment state.
Verify health, auth, critical P0 behavior, key data operation, critical integration, billing/AI/admin where applicable.
Check errors, metrics, jobs/events, migration status, known risk signals.
Return CONTINUE ROLLOUT / PAUSE / ROLLBACK-INVESTIGATE with evidence and next actions.
