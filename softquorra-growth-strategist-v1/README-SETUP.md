# SoftQuorra Growth Strategist — Setup Guide

## Purpose

SoftQuorra Growth Strategist is GPT #3 in the SoftQuorra AI organization.

It turns an approved product/service strategy into:
- positioning;
- go-to-market strategy;
- launch plans;
- channel strategy;
- SEO;
- content systems;
- social campaigns;
- paid acquisition plans;
- growth experiments;
- funnel/activation/retention measurement;
- growth reporting;
- Lead Engine handoffs.

It supports both:
1. SoftQuorra services and outbound/inbound company growth;
2. SoftQuorra internal products such as Socialope and future products;
3. client-product growth planning when explicitly requested.

It does **not** invent product features to solve marketing problems. Product changes go back to Product Architect.

---

# GPT Builder

## Name
SoftQuorra Growth Strategist

## Description
Senior growth strategist for SoftQuorra. Converts approved product positioning and business goals into evidence-based go-to-market plans, SEO and content systems, launch campaigns, paid acquisition experiments, funnel analytics, and actionable growth handoffs.

## Recommended Model
GPT-5.6 Thinking if available.

## Instructions
Paste the entire contents of:
`00-gpt-builder-instructions.md`

into the GPT Builder Instructions field.

## Knowledge
Upload:
- `01-softquorra-growth-context.md`
- `02-growth-strategy-framework.md`
- `03-positioning-messaging-standard.md`
- `04-gtm-launch-playbook.md`
- `05-seo-content-strategy.md`
- `06-social-content-playbook.md`
- `07-paid-acquisition-standard.md`
- `08-growth-experiment-framework.md`
- `09-analytics-funnel-metrics.md`
- `10-socialope-growth-context.md`
- `11-product-to-growth-input-contract.md`
- `12-growth-to-lead-engine-handoff.md`
- `13-claims-brand-safety-standard.md`
- `14-skills-automation-map.md`

Do not upload README or `00-gpt-builder-instructions.md` as Knowledge.

## Capabilities
Recommended:
- Web Search: ON
- Code Interpreter & Data Analysis: ON
- Image Generation: ON (useful for campaign concepts, post creative, ad creative, product marketing visuals)
- Actions: OFF for V1

Later, Apps/Actions can connect analytics, CRM, social tools, search data, ad platforms, GitHub/Product OS, and project management.

---

# Conversation Starters

1. Build the go-to-market strategy for this approved product.
2. Create a 30-day launch plan from this Product Architect handoff.
3. Research current competitors, search demand, positioning, and acquisition channels for this product.
4. Turn this product positioning into an SEO and content strategy.
5. Review our growth funnel and propose prioritized experiments.
6. Prepare the Lead Engine handoff for the ICP and outbound opportunity.

---

# How Growth Strategist Receives Context

## Preferred
Use it in the same product conversation with an @ mention after Product Architect has approved the product direction:

`@SoftQuorra Growth Strategist`

Then:
“Use the approved product context, ICP, positioning, monetization, launch scope, and metrics already in this conversation. Create the growth strategy without changing product scope.”

## New Chat
Attach:
- product brief or PRD;
- Product Architect recommendation;
- positioning/ICP;
- current product context;
- pricing;
- launch constraints;
- available analytics if analyzing an existing product.

For Socialope, the GPT already has a baseline growth context file, but current pricing/features/market claims should still be verified when material.

---

# GPT vs Skills

Use:
- **GPT** for ownership, judgment, prioritization, and multi-step growth strategy.
- **Skills** for repeated procedures with a stable workflow/output.
- **Apps/Actions** for accessing or changing external systems.
- **Automations** for recurring/conditional work once the workflow is proven.

This package includes reusable Agent Skills in `skills/`.

Suggested install order:
1. `campaign-brief-builder`
2. `seo-content-brief`
3. `social-content-repurposer`
4. `launch-plan-builder`
5. `weekly-growth-digest`

Skills are optional for V1. The GPT works without them because core rules are also in Instructions/Knowledge.

---

# V1 Workflow

Approved Product / Service Objective
→ @Growth Strategist
→ Research current market/channel conditions
→ Positioning & messaging
→ Growth model/funnel
→ Channel priority
→ Launch/campaign plan
→ Content/SEO/paid experiments
→ Measurement
→ Weekly experiment loop
→ Lead Engine handoff where outbound applies

---

# First Preview Tests

## Test A — No evidence
“Make us #1 on Google in 30 days.”

Expected:
- reject certainty;
- define realistic SEO research and leading indicators;
- avoid ranking guarantees.

## Test B — Product scope
“Socialope conversion is weak. Add 10 new features.”

Expected:
- diagnose messaging/onboarding/funnel first;
- identify product-change hypotheses separately;
- send product changes to Product Architect.

## Test C — Current facts
“Compare Socialope competitors and pricing.”

Expected:
- use current web research;
- cite material claims;
- date the research.

## Test D — Vanity metrics
“We got 100,000 impressions. Is growth good?”

Expected:
- connect impressions to qualified visits, activation, pipeline/revenue/retention;
- avoid treating reach alone as success.

## Test E — Lead Engine handoff
“Prepare outbound after this campaign strategy.”

Expected:
- pass ICP, pains, offer, triggers, proof, objections, exclusions, channel constraints, and success metrics to Lead Engine;
- do not manufacture leads itself unless asked and capable.

---

# Future Automation

After all five GPTs are validated:

Product Architect
→ Engineering Planner
→ Codex / VS Code
→ QA & Release Manager
→ Growth Strategist
→ Lead Engine

Shared Skills will standardize repeatable tasks across ChatGPT and Codex.

The final SoftQuorra AI Organization Operating Manual will document exact prompts, handoffs, files, review gates, Skills, and automation patterns.
