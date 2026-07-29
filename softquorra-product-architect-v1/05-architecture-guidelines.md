# SoftQuorra Architecture Guidelines

## Goal
Design systems that are simple enough to ship and operate, strong enough for real production use, and capable of evolving with validated demand.

Architecture is a product/economic decision, not a diagramming exercise.

---

# 1. Architecture Inputs

Before choosing a stack capture:
- product/business objective;
- primary user journeys;
- expected user/tenant count;
- traffic shape and peak assumptions;
- data shape and sensitivity;
- tenancy;
- offline/realtime requirements;
- background/scheduled work;
- integrations;
- AI workload;
- latency expectations;
- availability/recovery needs;
- geographic/data residency constraints;
- team size/skills;
- budget and unit economics;
- launch timeline;
- operational owner.

If unknown, label assumptions.

---

# 2. Technology Choice

SoftQuorra has preferred technologies in `02-technology-standards.md`.

**Preferred technology does not mean mandatory technology.**

Choose based on requirements and total ownership cost. A non-preferred technology is acceptable when it clearly improves product fit, platform compatibility, security, performance, staffing, ecosystem, or economics.

Record significant deviations/choices in an ADR.

---

# 3. Simplicity First

Default question:
“What is the smallest credible production architecture for the current validated scope?”

Often suitable for MVP:
- Next.js/React client;
- NestJS application/API;
- PostgreSQL;
- managed authentication;
- object storage;
- managed queue/background jobs;
- selected external APIs;
- managed deployment;
- basic observability.

This is an example, not a mandatory reference architecture.

Avoid adding:
- microservices;
- Kubernetes;
- event buses;
- multiple databases;
- service mesh;
- multi-region;
- vector databases;
- custom auth;
- custom schedulers;
unless a real requirement justifies them.

---

# 4. Modular Monolith vs Microservices

Prefer modular monolith when:
- one/small team owns the product;
- domains can be separated in code;
- independent scaling is not needed;
- deployment coordination is manageable;
- speed and operational simplicity matter.

Consider service extraction when:
- workload has materially different scaling;
- independent reliability boundaries are required;
- different teams own domains;
- security/data boundaries require separation;
- release cadence requires independence;
- specialized runtimes are needed.

Do not split services merely because the product may grow.

---

# 5. Domain Boundaries

Even inside a monolith:
- define domain modules;
- avoid arbitrary cross-domain data access;
- give entities clear ownership;
- expose domain services/contracts;
- prevent business logic from accumulating in controllers/UI;
- keep external-provider code behind integration boundaries.

Typical domains:
Identity, Organization/Tenant, Billing, Content, Projects, Integrations, AI, Notifications, Analytics, Administration.

Domains vary by product.

---

# 6. Data Architecture

For each data domain decide:
- system of record;
- owner;
- tenant boundary;
- consistency need;
- lifecycle;
- retention/deletion;
- audit need;
- sensitive classification;
- access patterns;
- indexing;
- backup/recovery;
- migration.

Prefer PostgreSQL for relational product data unless another data model is clearly better.

Use caching only when:
- latency/load evidence warrants it;
- stale-data behavior is understood;
- invalidation strategy exists.

---

# 7. Multi-Tenancy

Choose tenant model intentionally.

Common approaches:
- shared DB/shared schema with tenant IDs;
- shared DB/separate schema;
- database per tenant.

Evaluate:
- isolation;
- compliance;
- scale;
- customer customization;
- backup/restore;
- operational cost.

Every tenant-owned query must enforce tenant scope at a reliable boundary.

---

# 8. APIs

Define:
- consumer;
- resource/domain;
- authentication;
- authorization;
- validation;
- error contract;
- idempotency;
- pagination;
- version/evolution strategy;
- rate limits;
- observability.

Use synchronous API calls for interactive work. Use jobs/events when work is slow, retryable, scheduled, or decoupled.

---

# 9. Integrations

External services fail.

For every critical integration define:
- authentication;
- secrets;
- timeouts;
- retry policy;
- rate limit behavior;
- idempotency;
- webhook verification;
- duplicate/out-of-order events;
- provider outage behavior;
- user-facing status/error;
- reconciliation;
- vendor exit strategy.

---

# 10. Background Jobs

Use queues/jobs for:
- email/notifications;
- AI processing beyond normal request latency;
- large imports;
- external sync;
- scheduled automation;
- retryable work.

Jobs should be:
- idempotent where possible;
- observable;
- retry-limited;
- dead-letter/failed-state aware;
- cancellable where product semantics require;
- associated with user/tenant context.

---

# 11. AI Architecture

Separate:
1. deterministic application logic;
2. model invocation;
3. tool/integration layer;
4. context/retrieval;
5. orchestration/state;
6. evaluation/telemetry;
7. approval/fallback.

Use AI only where probabilistic behavior adds value.

Do not give a model broad production privileges by default. Use scoped tools and approval for high-impact actions.

---

# 12. Build vs Buy

Prefer managed/commodity services when they:
- reduce risk;
- reduce time-to-market;
- improve compliance/security;
- have acceptable economics;
- provide a credible migration path.

Evaluate build-vs-buy for:
- auth;
- payments;
- email;
- storage/CDN;
- monitoring;
- analytics;
- search;
- notifications;
- feature flags;
- queues;
- AI/model hosting.

---

# 13. Reliability

Classify workflows by business criticality.

Define:
- acceptable failure;
- timeout;
- retries;
- consistency;
- recovery;
- backup;
- monitoring;
- human remediation.

Do not impose enterprise-grade availability targets on low-risk MVP workflows without business justification.

---

# 14. Performance

Set performance targets from user experience and workload.

Measure:
- client loading/interactivity;
- API latency;
- DB query performance;
- queue wait/processing time;
- AI latency;
- integration latency.

Use percentile targets where mature enough. Do not invent thresholds; benchmark or define product expectations.

---

# 15. Security & Privacy

Use `11-security-and-privacy-standards.md`.

Architecture must show:
- trust boundaries;
- identities;
- permissions;
- tenant isolation;
- sensitive data paths;
- secret storage;
- external data sharing;
- public/private surfaces;
- administrative access.

---

# 16. Observability

At minimum for production-critical paths consider:
- structured logs;
- error tracking;
- metrics;
- traces where distributed flows justify them;
- job state;
- external API failures;
- deployment visibility;
- security/audit events where required.

Define actionable alerts, not alert noise.

---

# 17. Deployability

Define:
- local/dev/test/staging/prod approach;
- CI checks;
- migration execution;
- secrets/config;
- deploy method;
- rollback/redeploy;
- feature flags if risky;
- seed/test data;
- environment parity where material.

---

# 18. Quality Dimensions

Review every material architecture against:

1. Product fit
2. Developer velocity
3. Maintainability
4. Security/privacy
5. Reliability
6. Performance
7. Scalability
8. Cost efficiency
9. Operational excellence
10. Observability
11. Data integrity
12. Accessibility impact
13. Vendor lock-in/exit path
14. Sustainability/resource efficiency where relevant
15. AI reliability where relevant

Document meaningful tradeoffs.

---

# 19. Diagram Standard

## System Context
Show:
- users/actors;
- product/system;
- important external systems.

## Container
Show:
- web/mobile apps;
- backend/services;
- database;
- queues;
- storage;
- AI/model services;
- key external providers.

## Component
Use only where a complex/risky subsystem benefits.

Prefer Mermaid for portable documentation.

---

# 20. Architecture Review Checklist

- Does architecture map to approved P0 scope?
- Are assumptions visible?
- Is there unnecessary complexity?
- Are trust/tenant boundaries clear?
- Is the source of truth clear?
- Are external failures handled?
- Are high-cost AI/API paths modeled?
- Is build-vs-buy justified?
- Are critical risks observable?
- Can the team deploy/operate it?
- Is there a credible migration path if scale changes?
- Are significant decisions recorded as ADRs?
