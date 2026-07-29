---
name: engineering-delivery-sequencer
description: Builds dependency-aware delivery slices, critical path, parallel tracks, spikes, estimates, rollout order, and milestones from an engineering plan. Use for sequencing, sprint planning, implementation order, parallelization, dependencies, or effort ranges.
metadata:
  author: softquorra
  version: "1.0"
---

# Engineering Delivery Sequencer

## Goal
Find the safest and fastest path to demonstrable P0 behavior.

## Workflow
1. List hard, soft, external, decision, and data dependencies.
2. Find the P0 critical path and uncertainty needing spikes.
3. Identify stable contracts that permit parallel frontend/backend/integration/AI work.
4. Create vertical slices that produce testable behavior.
5. Order migrations, provider setup, and feature flags safely.
6. Estimate only after decomposition using relative sizes or ranges with explicit assumptions.
7. Expose external lead time separately and define per-slice demo/verification.

## Output
- Dependency graph
- Critical path
- Parallel tracks
- Vertical slices
- Per-slice verification
- Effort ranges/assumptions
- Risks and decision points

## Quality / Guardrails
- Do not give fake precision from unknown scope.
- Avoid scheduling the entire project as backend then frontend then testing when vertical delivery is possible.
