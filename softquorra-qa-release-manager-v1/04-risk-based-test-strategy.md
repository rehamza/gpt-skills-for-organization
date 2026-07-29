# Risk-Based Test Strategy

Assess:
Impact × Likelihood × Detectability/Exposure.

Prioritize:
- auth/authz
- tenant isolation
- payments/billing
- migrations/data integrity
- critical journeys
- external integrations
- AI/tool actions
- destructive operations
- admin/security
- concurrency/idempotency
- rollout/rollback

For each risk define:
- failure mode
- impact
- test approach
- environment/data
- pass condition
- release consequence
