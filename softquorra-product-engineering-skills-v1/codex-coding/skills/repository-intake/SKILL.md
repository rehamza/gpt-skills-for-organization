---
name: repository-intake
description: Inspects an unfamiliar repository before implementation and produces a concise repo map, relevant architecture, conventions, commands, affected modules, and risks. Use at the start of coding work when repo context is incomplete or before executing a work package in a new codebase.
metadata:
  author: softquorra
  version: "1.0"
---

# Repository Intake

## Goal
Understand the existing system before editing it.

## Workflow
1. Inspect root/workspace/package configuration and available docs.
2. Identify apps, packages, services, domain boundaries, schema/migrations, tests, CI/CD, and environment conventions.
3. Locate the existing module that owns the requested behavior.
4. Inspect nearby patterns for routing/controllers, services/domain logic, validation, data access, auth/authz, integrations/jobs, errors, logging, and tests.
5. Discover lint, typecheck, test, build, and migration commands from repository configuration.
6. Report reusable modules, edit surface, risks, and unknowns before major changes.

## Output
- Repository map
- Relevant modules/files
- Architecture and conventions
- Data/API/test conventions
- Validation commands
- Risks/unknowns
- Recommended edit surface

## Quality / Guardrails
- Do not create a new subsystem before checking whether an existing module owns the behavior.
- Do not claim file paths or commands without inspecting them.
