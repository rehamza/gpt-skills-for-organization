---
name: qa-handoff-readiness-check
description: Validates whether an engineering QA handoff, implementation completion evidence, build, and approved requirements are sufficient to begin QA and release verification. Use when QA receives a new release candidate, engineering handoff, or implementation package.
metadata: {author: softquorra, version: "1.0"}
---
# QA Handoff Readiness Check
1. Identify release/build, PRD version, P0 scope, acceptance criteria, and implementation evidence.
2. Check migrations, integrations, AI, security, observability, flags, rollout, known risks.
3. Separate blocking missing information from non-blocking TBDs.
4. State which areas can be tested now.
5. Return READY / READY WITH NON-BLOCKING TBDS / PARTIALLY READY / NOT READY.
Do not invent missing acceptance criteria.
