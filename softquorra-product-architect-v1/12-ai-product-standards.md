# SoftQuorra AI Product Standards

## Purpose
Ensure AI is used where it creates real product value and that AI features are measurable, safe, economical, and operable.

---

# 1. AI Justification

Before selecting a model answer:
- what exact user problem requires AI?
- what part is probabilistic?
- could deterministic rules/search/workflow solve it more reliably/cheaply?
- what value does AI add?
- what happens when it is wrong?

AI is a capability, not a product strategy by itself.

---

# 2. AI Feature vs Agent

## AI Feature
A bounded model call or workflow such as:
- summarize;
- classify;
- extract;
- rewrite;
- generate draft;
- rank.

## AI Agent
A system where a model participates in deciding steps and using tools toward a goal, usually with state, constraints, and feedback.

An agent should have clearly defined:
- goal;
- state/context;
- tools;
- decision boundary;
- termination condition;
- guardrails;
- permissions;
- approval;
- observability.

Do not call every LLM request an agent.

---

# 3. Task Specification

For each AI task document:
- task ID;
- user;
- trigger;
- input;
- required context;
- output;
- output schema;
- quality criteria;
- unacceptable behavior;
- latency expectation;
- fallback;
- human approval;
- data classification.

---

# 4. Model Selection

Evaluate:
- task quality;
- structured-output/tool capability;
- context needs;
- latency;
- cost;
- privacy/data terms;
- availability;
- regional constraints;
- vendor lock-in;
- rate limits.

Do not choose a model only because it is newest/largest.

Where practical, wrap provider access behind a product-level interface without over-abstracting prematurely.

---

# 5. Prompt & Version Management

Treat important prompts as product artifacts.

Track:
- prompt identifier/version;
- model/settings;
- expected schema;
- examples;
- eval results;
- deployment date.

Changing prompt/model can be a production behavior change. Regression test material workflows.

---

# 6. Structured Outputs

Prefer schema-constrained output for data used programmatically.

Validate:
- required fields;
- types;
- enumerations;
- max lengths/ranges;
- references/IDs;
- permission-safe tool arguments.

Model output is untrusted until validated.

---

# 7. Retrieval / RAG

Use retrieval only when external/private/current knowledge must ground the task.

Before adding vector search ask whether:
- SQL filters;
- full-text search;
- API lookup;
- direct document selection;
would solve it more simply.

RAG design covers:
- source authority;
- document permissions;
- chunk/index approach;
- freshness;
- citations/provenance;
- retrieval evaluation;
- stale/deleted content;
- tenant isolation.

Never let retrieval bypass user permissions.

---

# 8. Tools & Actions

For every tool define:
- purpose;
- permission;
- input schema;
- validation;
- side effect;
- idempotency;
- rate/spend limit;
- error behavior;
- audit event;
- approval requirement.

The model must not decide authorization. The tool/backend must enforce it.

---

# 9. Autonomy Levels

Suggested model:

### Level 0 — Suggest
AI produces information/draft only.

### Level 1 — Approve Then Act
AI prepares an action; user explicitly approves.

### Level 2 — Bounded Automation
AI acts automatically inside narrow rules/limits; user can review/stop.

### Level 3 — High Autonomy
AI chooses and executes broader actions.

Use the lowest autonomy that still creates product value.

High-impact actions involving money, external communication, deletion, permissions, sensitive data, or irreversible changes should generally require stronger controls/approval.

---

# 10. Failure & Fallback

Plan for:
- model timeout;
- provider outage;
- rate limit;
- invalid structure;
- hallucination;
- unsafe request;
- tool failure;
- partial completion;
- duplicate action;
- runaway loop/cost.

Fallback options:
- retry with limit;
- alternative model;
- deterministic fallback;
- human review;
- save as draft;
- queue for later;
- transparent failure.

Never create infinite autonomous retry loops.

---

# 11. Evaluation

Define evals before production.

Possible dimensions:
- task success;
- correctness;
- relevance;
- groundedness;
- hallucination/fabrication;
- extraction/classification F1/accuracy where appropriate;
- tool selection;
- tool-call success;
- schema validity;
- human approval rate;
- edit distance/amount of human correction;
- latency;
- cost per successful task;
- user satisfaction;
- safety/abuse.

Use a representative evaluation set, including edge/failure cases.

---

# 12. Human Evaluation

For subjective tasks define a rubric.

Example 1–5:
1. unusable/wrong
2. major rewrite
3. acceptable with edits
4. good/minor edits
5. ship-ready

Track inter-rater differences when evaluation matters materially.

---

# 13. AI Observability

Capture enough to debug and measure while respecting privacy.

Potential fields:
- workflow/task ID;
- model/provider;
- prompt version;
- token/usage;
- latency;
- tool calls;
- retrieval sources;
- schema failures;
- retry;
- user approval/edit/reject;
- final outcome;
- cost.

Do not log sensitive content by default without a need and controls.

---

# 14. Cost Controls

Model:
- calls per workflow;
- average input/output;
- model cost;
- search/tool cost;
- retries;
- background runs;
- customer usage distribution.

Controls:
- limits;
- quotas/credits;
- caching where semantically safe;
- smaller models for simpler tasks;
- batching where appropriate;
- timeout/max steps;
- spend alert.

Optimize cost per successful user outcome, not merely cost per token.

---

# 15. AI Privacy & Data

Determine:
- what user/client data is sent;
- provider retention/training terms;
- region;
- secrets/credentials exposure;
- sensitive data;
- retrieval permission;
- deletion behavior;
- customer disclosure/consent where required.

Verify current provider terms instead of assuming.

---

# 16. Safety / Abuse

Consider:
- spam;
- impersonation;
- harmful automation;
- unauthorized data collection;
- policy/platform violations;
- prompt injection;
- malicious uploaded content;
- excessive outreach/actions.

Product safeguards should be built into tools, permissions, quotas, approval, and monitoring—not prompt text alone.

---

# 17. Release Gate

An AI feature is ready only when:
- use case is clear;
- failure behavior is acceptable;
- evaluation exists;
- release threshold is met;
- privacy/security reviewed;
- cost modeled;
- observability exists;
- approval/autonomy is defined;
- fallback exists;
- provider dependency is understood.
