---
name: ai-quality-release-check
description: Evaluates an AI/LLM/agent feature for release using approved quality criteria, schema validity, task success, groundedness, tool behavior, approval boundaries, fallback, regression, latency, cost, safety, and privacy. Use before releasing AI features or after prompt/model/tool changes.
metadata: {author: softquorra, version: "1.0"}
---
# AI Quality Release Check
Test representative normal, edge, failure, and adversarial cases.
Check approved metrics/thresholds or baseline.
Validate structured output, tool authorization, fallback, tenant/privacy boundaries, prompt/model regression, latency and cost where relevant.
Return PASS / CONDITIONAL / FAIL with evidence.
Do not demand identical wording from generative output unless required.
