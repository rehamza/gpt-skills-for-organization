# SoftQuorra Product Research & Validation Framework

## Objective
Convert a product idea or client problem into an evidence-backed decision before expensive engineering begins.

The purpose of research is not to produce a long report. It is to reduce uncertainty around the questions that could change the build/no-build, scope, customer, monetization, or architecture decision.

---

# 1. Intake

Capture:
- product/client name;
- idea in one sentence;
- requested outcome;
- who proposed it;
- known users/customers;
- geography/industry;
- expected platform;
- deadline/budget if known;
- known integrations/data;
- constraints;
- existing evidence;
- decisions the research must support.

## Intake Output
**Decision question:** What are we trying to decide?

Examples:
- Should SoftQuorra build this internal product?
- Which ICP should the MVP target?
- Is AI necessary?
- Which platform should launch first?
- Which client workflow should be automated first?

---

# 2. Problem Discovery

Define:
- problem;
- user/person experiencing it;
- trigger;
- frequency;
- severity;
- current workflow;
- workaround;
- cost of current behavior;
- why now;
- consequence of doing nothing.

## Problem Evidence Hierarchy
Strong:
- user interviews with repeated pain;
- transaction/usage/support data;
- paid demand/preorders/contracts;
- observed workflow;
- repeated search/community behavior;
- customer request patterns.

Medium:
- competitor adoption;
- credible market studies;
- active communities discussing the pain;
- repeated public reviews/complaints.

Weak:
- founder intuition only;
- broad trend headlines;
- “AI is growing”;
- competitor feature existence without evidence users value it.

---

# 3. Customer / ICP

Define the narrowest useful initial ICP.

For B2B:
- industry;
- company size;
- team/function;
- workflow maturity;
- current tools;
- pain trigger;
- budget authority;
- buyer;
- end user;
- geography/compliance needs.

For B2C:
- behavior/context;
- frequency of problem;
- existing spend;
- skill level;
- motivation;
- platform;
- acquisition channel.

Avoid demographic detail that does not affect product behavior.

---

# 4. Jobs To Be Done

Format:
**When [situation], I want to [motivation/action], so I can [desired outcome].**

Capture:
- functional job;
- emotional job where relevant;
- social job where relevant;
- trigger;
- desired outcome;
- current workaround;
- switching barriers.

---

# 5. Existing Alternatives

Research more than direct competitors.

Include:
- direct competitors;
- adjacent products;
- spreadsheets/manual workflows;
- agencies/freelancers;
- internal staff;
- open source;
- platform-native features;
- general AI assistants;
- “do nothing.”

For each relevant alternative:
- ICP;
- value proposition;
- core workflow/features;
- pricing/business model;
- distribution;
- strengths;
- weaknesses;
- switching costs;
- user complaints/praise where credible;
- implications for SoftQuorra.

---

# 6. Competitive Matrix

Recommended columns:
| Competitor | ICP | Core job | Price/value metric | Key capability | Differentiator | Weakness/gap | Evidence date |

Do not use a feature matrix alone to claim differentiation.

Good differentiation may come from:
- narrower ICP;
- stronger workflow integration;
- faster time-to-value;
- proprietary data;
- trusted distribution;
- lower operational burden;
- collaboration;
- automation;
- better economics;
- improved quality/reliability;
- regulatory/domain specialization.

---

# 7. Market Assessment

Determine:
- category;
- maturity;
- growth/decline signals;
- buyer behavior;
- major trends;
- regulatory/platform forces;
- consolidation/fragmentation;
- distribution structure.

## TAM/SAM/SOM
Only calculate when inputs are defensible.

### Top-down
Use credible category data but explain why the category maps to the actual product.

### Bottom-up
Prefer when possible:
number of target customers × plausible annual contract/value.

Always list:
- data source;
- year;
- calculation;
- assumptions;
- sensitivity/range.

Never present false precision.

---

# 8. Demand & Willingness to Pay

Look for:
- existing spend on alternatives;
- budget line ownership;
- paid competitors;
- paid pilots;
- user statements tied to actual behavior;
- waitlist/preorder/deposit;
- inbound requests;
- conversion from manual service;
- measurable time/revenue/risk savings.

A “like” or survey interest is weaker than actual behavioral evidence.

---

# 9. Distribution Assessment

For each likely acquisition path capture:
- channel;
- ICP availability;
- CAC difficulty;
- sales cycle;
- trust requirement;
- content/search demand;
- partnership possibility;
- marketplace/platform dependency;
- outbound feasibility;
- product-led loop;
- referral/network effects if real.

A product with strong technology but no credible path to customers is not validated.

---

# 10. Monetization Inputs

Capture:
- who pays;
- value received;
- frequency of value;
- measurable value metric;
- current spend;
- competitor pricing;
- variable costs;
- gross-margin risks;
- potential upgrade triggers;
- enterprise requirements.

Use `06-monetization-framework.md` for full analysis.

---

# 11. Technical Feasibility

Assess:
- platform/client apps;
- data sources;
- data quality/rights;
- external API availability;
- rate limits;
- realtime/background needs;
- AI fit;
- model limitations;
- latency;
- expected load;
- integrations;
- security/privacy;
- offline/native requirements;
- operational burden;
- likely architecture;
- proof-of-concept needs.

Classify:
- straightforward;
- moderate uncertainty;
- high uncertainty / spike required.

---

# 12. AI Feasibility

If AI is proposed, test:
- can deterministic logic solve this better?
- what exact task is probabilistic?
- what data/context is available?
- what is an acceptable failure?
- does a human approve?
- what is the cost per successful outcome?
- how will quality be evaluated?
- can the provider/model meet privacy/latency needs?

Use `12-ai-product-standards.md`.

---

# 13. Risk Register

Categories:
- market;
- customer;
- differentiation;
- distribution;
- monetization;
- technical;
- data;
- AI;
- platform/vendor;
- security/privacy;
- legal/compliance;
- operational;
- financial.

For each:
Risk | Likelihood | Impact | Evidence | Mitigation | Validation action.

---

# 14. Validation Experiments

Prefer the cheapest experiment capable of invalidating a risky assumption.

Examples:
- 10–15 focused interviews;
- concierge/manual service;
- clickable prototype;
- landing page + qualified traffic;
- paid pilot;
- design partner LOI;
- API/AI technical spike;
- fake-door test where ethically appropriate;
- pricing interview;
- demo + commitment request.

Define before running:
- hypothesis;
- method;
- target sample;
- success threshold;
- failure threshold;
- timeframe;
- decision after result.

Do not move thresholds after seeing results without documenting why.

---

# 15. Recommendation

Output one:
- **GO**
- **GO WITH CONDITIONS**
- **VALIDATE FIRST**
- **PIVOT**
- **DO NOT BUILD**

Include:
1. decision;
2. strongest supporting evidence;
3. strongest contradictory evidence;
4. biggest unknowns;
5. score from `14-product-scorecard.md` if enough evidence exists;
6. smallest next action;
7. what must become true before engineering starts.

---

# Research Source Log

For important evidence keep:

| Claim | Source | Source type | Date accessed | Confidence | Notes |
|---|---|---|---|---|---|

Use current web research for facts that can change.
