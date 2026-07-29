# SoftQuorra Engineering Technology Standards

## Core Rule
**Preferred technology does not mean mandatory technology.**

Use this stack as a proven default. Follow approved architecture first. Recommend alternatives when requirements justify them.

## Languages
- TypeScript for most web/backend product work
- Python for AI/data workloads where ecosystem or runtime fit is stronger

## Frontend
Preferred:
- React
- Next.js App Router
- TypeScript
- Tailwind CSS
- Ant Design where appropriate
- TanStack Query
- Zustand where appropriate

Planning should identify route/screen, server/client responsibility, API dependency, state ownership, validation, loading/error/empty states, accessibility, and analytics.

## Backend
Preferred:
- Node.js
- NestJS
- TypeScript
- REST APIs
- FastAPI/Python for justified AI/data services

Prefer modular monolith for many MVPs. Extract services when scaling, reliability, security, runtime, or ownership boundaries justify it.

## Database
Preferred:
- PostgreSQL
- Prisma
- Supabase where useful
- Redis for cache/coordination/queues, not default durable truth

Plan constraints, indexes, tenancy, migration, backfill, rollback/compatibility, retention, and deletion.

## Authentication
Proven:
- Supabase Auth
- OAuth2/OIDC
- JWT/session approaches
- managed identity providers

Do not implement custom authentication without strong justification.

Authorization must be enforced server-side and include resource/tenant scope.

## Background Work
Preferred:
- BullMQ
- Redis
- managed queue/job systems where appropriate

Plan idempotency, retry limits, failed states, observability, cancellation if required, and tenant/user context.

## AI
Proven:
- OpenAI
- Anthropic
- Mastra
- LangGraph
- LangChain
- Python orchestration
- structured outputs/tool calling
- RAG where required

AI planning must include evals, cost, latency, fallback, permission boundaries, and telemetry.

## Mobile
Preferred:
- React Native

Plan navigation/screens, network/offline behavior, deep links, push notifications, permissions, native modules, and store/runtime constraints.

## Payments
Preferred:
- Stripe where appropriate

Plan verified webhooks, idempotency, entitlement mapping, cancellation/refund, and reconciliation.

## DevOps
Proven:
- Docker
- Vercel
- Railway
- CI/CD
- Nx monorepos where justified

Plan environments, secrets, CI gates, migrations, deploy, rollback, monitoring, and backups.

## Avoid Unless Justified
- premature microservices;
- Kubernetes for small systems;
- multiple databases without workload need;
- event buses without real async/domain need;
- vector DB when SQL/search is enough;
- custom auth/billing;
- large rewrites instead of incremental migration;
- abstractions before repeated need;
- repository paths invented without repo context.
