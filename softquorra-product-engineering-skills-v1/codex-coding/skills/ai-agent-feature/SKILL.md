---
name: ai-agent-feature
description: Implements an approved AI/LLM or agent feature with structured outputs, prompt/version management, tool authorization, evals, fallback, cost/latency controls, and observability. Use for OpenAI/Anthropic calls, Mastra, LangGraph, LangChain, RAG, tool calling, generation, classification, or agent workflows.
metadata:
  author: softquorra
  version: "1.0"
---

# Ai Agent Feature

## Goal
Implement measurable and bounded AI behavior rather than uncontrolled model calls.

## Workflow
1. Confirm the approved AI task, input/output, autonomy/approval, and why probabilistic behavior is required.
2. Inspect existing model/provider abstractions, prompt conventions, tools, retrieval, and telemetry.
3. Implement the smallest workflow that satisfies the task.
4. Version important prompt/agent instructions and schema-validate outputs consumed by code.
5. Enforce backend authorization inside tools/actions and scope side effects.
6. Implement timeouts, retry/max-step/spend limits, fallback, and approval as required.
7. Protect tenant/private context and retrieval permissions.
8. Add representative eval/regression cases and telemetry for provider/model, prompt version, latency, failures, tools, and cost where approved.
9. Run tests/evals and report limitations.

## Output
- AI implementation
- Prompt/schema/tool changes
- Approval/fallback
- Evals
- Telemetry
- Cost/latency considerations
- Validation results

## Quality / Guardrails
- Do not add RAG when SQL/full-text/direct lookup is enough.
- Do not turn a bounded LLM call into an autonomous agent without approved design.
- Treat model output as untrusted until validated.
