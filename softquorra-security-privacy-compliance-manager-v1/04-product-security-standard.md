# Product Security Standard

Convert risk into testable requirements, using current stable OWASP ASVS where applicable.

## Core Areas

Identity: secure registration/recovery, MFA/passkeys when needed, session protection, credential rate limits, OAuth scope control and reauthentication.

Authorization: server-side checks, deny by default, tenant/resource ownership, roles, admin separation and object-level tests.

Multi-tenancy: tenant enforcement across queries, storage, cache, jobs, queues and support access; cross-tenant regression tests.

Data: classification, encryption, secret storage, redaction, secure deletion, backups and restricted production access.

Input/output: schema validation, injection prevention, safe uploads, output encoding, SSRF/path traversal and deserialization protections.

APIs/webhooks: authentication, signatures, replay prevention, idempotency, limits, timeouts/retries, dedupe/order and reconciliation.

Logging: never log secrets/tokens/passwords/unnecessary personal data; audit sensitive actions.

Availability/abuse: quotas, rate/spend controls, graceful degradation and failure visibility.

Recovery: tested backups, restore, rollback/forward-fix and dependency failure plans.

Threat models identify assets, actors, trust boundaries, entry points, threats, abuse cases, controls, residual risk and tests.

Requirement example:
`SEC-AUTHZ-004 — Every request for a tenant-owned campaign must verify server-side that the authenticated user has the required role in that tenant.`
