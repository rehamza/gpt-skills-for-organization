---
name: frontend-feature
description: Implements an approved React/Next.js or existing frontend feature following repository design system, routing, state, data-fetching, validation, accessibility, error/loading/empty-state, analytics, and testing conventions. Use for web screens, forms, components, workflows, and client-side integration.
metadata:
  author: softquorra
  version: "1.0"
---

# Frontend Feature

## Goal
Deliver the approved user journey without creating a parallel frontend architecture.

## Workflow
1. Inspect current routes, components, design system, query/state, form, and test patterns.
2. Confirm journey, permissions, API contract, and acceptance criteria.
3. Reuse design-system primitives and existing state/data-fetching conventions.
4. Implement loading, empty, error, success, disabled, and permission states as relevant.
5. Validate forms at appropriate client/server boundaries.
6. Preserve accessibility: semantics, labels, keyboard/focus, and actionable errors.
7. Add required analytics events and component/integration/E2E tests.
8. Run lint, typecheck, tests, and build for the affected app.

## Output
- UI changes
- State/API integration
- Accessibility behavior
- Analytics
- Tests
- Validation results

## Quality / Guardrails
- Do not add a new state-management/component framework for a local feature without architectural approval.
- Do not hide permission failures or backend errors with optimistic UI only.
