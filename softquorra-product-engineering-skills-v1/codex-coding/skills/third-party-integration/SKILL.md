---
name: third-party-integration
description: Implements an approved third-party API, OAuth, webhook, email, billing, social-platform, or data-provider integration with auth, rate limits, retries, idempotency, reconciliation, failure handling, secrets, and tests. Use for Stripe, Resend, Supabase integrations, social APIs, data providers, and external services.
metadata:
  author: softquorra
  version: "1.0"
---

# Third Party Integration

## Goal
Integrate external providers safely under real provider constraints and failure modes.

## Workflow
1. Read the approved provider/use case and inspect existing integration patterns.
2. Verify current official SDK/API behavior when documentation access exists.
3. Implement credentials/secrets with existing secure configuration and exact required scopes.
4. Validate request/response payloads and map provider errors.
5. Implement timeout/retry only for retry-safe cases, idempotency for duplicate side effects, and rate-limit behavior.
6. For webhooks verify authenticity, handle duplicates/out-of-order events, queue slow work, and support failed-state reconciliation.
7. Implement user-facing outage/failure behavior.
8. Add unit/mocks plus sandbox/contract tests when available and provider observability where required.

## Output
- Integration implementation
- Auth/scopes/secrets handling
- Reliability behavior
- Webhook/reconciliation
- Tests
- Provider limits/assumptions
- Validation results

## Quality / Guardrails
- Do not rely on remembered API limits/scopes when current official docs are available.
- Do not log credentials or sensitive provider payloads.
