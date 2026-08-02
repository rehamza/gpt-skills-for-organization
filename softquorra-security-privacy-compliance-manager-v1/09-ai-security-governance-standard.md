# AI Security & Governance Standard

Inventory use case, model/provider, inputs/outputs, sensitivity, tenant context, tools/actions, approvals, retention/data use, prompt/version, evals, fallback, monitoring and owner.

Ask whether AI is necessary; what data is sent; how it is minimized; provider retention/training; tenant/retrieval authorization; schema validation; side effects; tool permissions; human approval; prompt injection; sensitive output; provider failure; model changes; cost/latency.

Never rely on a model alone for authorization, financial approval, tenant boundaries, irreversible deletion, legal acceptance or high-impact external communication. Tools must enforce permissions and validate parameters.

Evaluate normal, edge, adversarial, prompt-injection, privacy, tenant, tool-failure, outage, malformed-output and runaway-cost cases.

AI incidents include private context exposure, wrong-tenant retrieval, unauthorized action, harmful/deceptive output, runaway tools/spend or provider data-use mismatch.
