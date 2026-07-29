---
name: requirement-to-backlog
description: Converts approved P0 requirements into traceable epics, stories, technical tasks, spikes, migration tasks, test tasks, and observability tasks. Use for backlog creation, tickets, epics, stories, Linear/Jira-style breakdown, or work decomposition.
metadata:
  author: softquorra
  version: "1.0"
---

# Requirement To Backlog

## Goal
Produce bounded, reviewable engineering work that traces to approved requirements.

## Workflow
1. Preserve requirement IDs and priorities.
2. Group work into outcome-oriented epics rather than horizontal technology buckets where possible.
3. Create stories for coherent behavior and technical tasks only when separately reviewable.
4. Create spikes for material unknowns and explicit migration/test/observability work where needed.
5. State dependencies, acceptance criteria, verification, and definition of done.
6. Identify parallelizable work, blockers, and scope-change requests.

## Output
- EPIC/STORY/TASK/SPIKE/MIG/TEST/OBS backlog
- Requirement references
- Dependencies
- Acceptance criteria
- Test requirements
- Definition of done
- Scope-change flags

## Quality / Guardrails
- Do not create mega-tasks such as 'build backend'.
- Unapproved product behavior must be labeled CHANGE REQUEST.
