# SoftQuorra Technology Standards

## Principle
These technologies represent SoftQuorra’s **preferred and proven toolset**.

**Preferred technology does not mean mandatory technology.**

Architecture starts from requirements. The Product Architect may recommend a different technology when product, platform, security, performance, ecosystem, staffing, cost, or operational requirements justify it. The decision must explain the tradeoff.

Do not force a preferred stack into a problem it does not fit.

---

# Engineering Baseline

## Languages
Preferred:
- TypeScript for full-stack product/application development
- Python for AI/data/ML workloads and services where its ecosystem provides meaningful advantage

Use strong typing, explicit interfaces/contracts, and validation at boundaries.

## Web Frontend
Preferred:
- React
- Next.js with App Router
- TypeScript
- Tailwind CSS
- Ant Design where a component framework accelerates delivery
- TanStack Query for server-state workflows
- Zustand for lightweight client state where needed

Principles:
- accessible UI;
- responsive behavior;
- server/client boundaries chosen intentionally;
- avoid unnecessary global state;
- prefer reusable product primitives over copy-pasted screens.

## Backend
Preferred:
- Node.js
- NestJS
- TypeScript
- RESTful APIs as a default
- Python/FastAPI for AI/data services when justified

Architecture:
- modular monolith is the default starting point for many MVPs;
- extract services only when workload, ownership, reliability, deployment, or scaling needs justify it;
- keep domain boundaries explicit even inside a monolith.

## Authentication & Authorization
Proven options:
- JWT
- OAuth2/OIDC
- Supabase Auth
- managed identity providers where they reduce security/maintenance burden

Requirements:
- authentication and authorization are separate concerns;
- use least privilege;
- define tenant boundaries;
- model roles/permissions explicitly;
- do not implement custom authentication without a strong reason.

## APIs & Integrations
- REST by default when it fits the consumer and domain
- version or evolve contracts deliberately
- validate inputs/outputs
- verify webhook signatures
- idempotency for operations that may be retried
- retry with backoff only for appropriate failures
- protect against duplicate processing
- define timeout and failure behavior for third-party APIs

## Background Work
Preferred:
- Redis
- BullMQ
- provider-native queues/jobs when appropriate

Use background processing for:
- slow external integrations;
- emails/notifications;
- AI workloads that exceed interactive latency;
- scheduled jobs;
- retries;
- batch processing.

Do not add a queue merely for architectural fashion.

## Data
Preferred:
- PostgreSQL
- Prisma ORM
- Supabase when Auth/Realtime/Storage/Postgres integration accelerates delivery
- Redis for cache/ephemeral coordination, not as the default system of record

Principles:
- relational data belongs in relational structures unless requirements strongly indicate otherwise;
- use database constraints where they protect invariants;
- design indexes based on access patterns;
- use migrations;
- define ownership/tenancy;
- plan retention/deletion;
- avoid storing the same source-of-truth data in multiple systems without synchronization strategy.

## AI & Agents
Proven:
- OpenAI
- Anthropic
- Mastra
- LangGraph
- LangChain
- Python orchestration where appropriate
- structured outputs/tool calling
- RAG where retrieval is truly necessary

Rules:
- define the AI task before model/provider;
- prefer deterministic code for deterministic requirements;
- use agents only for workflows requiring model-driven decisions/tool use;
- define evals, fallback, cost, latency, approval, and observability;
- model providers should remain replaceable where economically/technically reasonable.

## Mobile
Preferred:
- React Native

Capabilities:
- iOS and Android
- native modules when necessary
- push notifications
- deep links
- app-store deployment
- performance profiling

Use native Swift/Kotlin/another framework when product requirements clearly justify it.

## Payments
Preferred:
- Stripe for billing/subscriptions/payments when available and appropriate

Principles:
- provider-hosted payment surfaces reduce PCI scope where possible;
- webhook events must be verified and idempotently processed;
- billing state and product entitlement state must be reconciled carefully.

## Email / External Services
Proven:
- Resend
- Serper
- other managed APIs where they improve speed and reliability

Vendor selection must consider:
- pricing;
- limits;
- data/privacy;
- reliability;
- lock-in;
- geographic availability;
- support;
- exit/migration path.

## Monorepo
Preferred when justified:
- Nx

Use monorepos when shared packages, coordinated releases, or multiple related apps/services benefit from them. Do not create workspace complexity for a tiny isolated project without benefit.

## DevOps
Proven:
- Docker
- CI/CD pipelines
- Vercel
- Railway
- managed cloud services

Production systems should define:
- environments;
- configuration/secrets;
- build/test/deploy pipeline;
- database migration approach;
- logs/metrics/traces as justified;
- backups/recovery;
- rollback/redeployment approach.

## Architecture Selection Rule
Before selecting technology, capture:
1. product type;
2. expected users/load;
3. data model;
4. realtime/background needs;
5. security/privacy/compliance;
6. integrations;
7. AI workload;
8. availability/latency needs;
9. budget/unit economics;
10. launch timeline;
11. team skills;
12. operational ownership.

Then choose the simplest credible stack.

## Avoid by Default Unless Justified
- microservices for early MVPs;
- Kubernetes for small products;
- event-driven architecture without a real async/domain need;
- vector databases when normal search/SQL is enough;
- custom authentication;
- custom billing;
- multiple databases without clear workload separation;
- premature multi-region architecture;
- speculative abstraction layers;
- technology chosen only because it is fashionable.

## Quality Principles
- readable maintainable code;
- small explicit modules;
- automated tests proportionate to risk;
- code review;
- security at boundaries;
- accessibility;
- observability for important workflows;
- safe migrations;
- feature rollout strategy for risky changes;
- documentation for important architecture decisions.
