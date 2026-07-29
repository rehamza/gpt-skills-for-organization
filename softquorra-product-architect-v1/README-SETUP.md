# SoftQuorra Product Architect — Setup Guide

## Purpose

SoftQuorra Product Architect is the product-discovery and architecture layer for SoftQuorra.

It accepts:
- a new internal product idea;
- a client product request;
- a feature proposal for an existing product;
- a product/market question;
- a technical architecture decision.

It produces:
- research and evidence;
- problem and ICP definition;
- competitor analysis;
- opportunity validation;
- MVP scope;
- monetization hypotheses;
- PRDs;
- architecture decisions and diagrams;
- risk analysis;
- an Engineering Planner handoff.

The GPT decides **what should be built and why**. The Engineering Planner later converts approved scope into epics, stories, implementation tasks, API/schema detail, and coding prompts.

---

# GPT Builder Configuration

## Name
SoftQuorra Product Architect

## Description
Senior product strategist and software architect for SoftQuorra. Researches and validates software and AI opportunities, defines MVP scope, creates production-grade PRDs, recommends monetization, designs technical architecture, and prepares projects for engineering.

## Instructions
Copy the complete contents of:

`00-gpt-builder-instructions.md`

into the GPT Builder **Instructions** field.

That file is intentionally kept below the 8,000-character editor limit.

## Knowledge
Upload files `01` through `14` as Knowledge.

Do **not** upload `00-gpt-builder-instructions.md` as a replacement for pasting it into Instructions. Instructions define behavior; the numbered files provide reference material and templates.

## Capabilities
Recommended:
- Web Search: ON
- Code Interpreter & Data Analysis: ON
- Image Generation: OFF for V1 unless visual ideation is needed
- Actions: OFF for V1

## Recommended Model
Choose the strongest reasoning model available in your GPT Builder model dropdown. Do not block the GPT from working if users select another supported model.

## Conversation Starters
1. Research and validate this product idea before we invest engineering time.
2. Turn this validated idea into a complete SoftQuorra PRD.
3. Review this PRD and identify product, market, technical, security, and architecture risks.
4. Design the smallest production-ready architecture for this product using SoftQuorra standards.
5. Analyze this client requirement and define the smallest credible solution SoftQuorra should propose.
6. Prepare the Engineering Planner handoff for this approved product.

---

# Knowledge File Order

01. Company truth and positioning
02. Technology preferences and engineering principles
03. Research/validation workflow
04. PRD template
05. Architecture principles
06. Monetization framework
07. Marketing/distribution context
08. Existing Socialope product context
09. ManaMind discovery workspace
10. Architecture Decision Record template
11. Security/privacy standard
12. AI product standard
13. Engineering handoff template
14. Opportunity scorecard

---

# First Preview Tests

Run these in the GPT Builder Preview before saving.

## Test A — Weak idea
“Build an AI CRM for every small business. Create the full PRD.”

Expected behavior:
- it should not blindly generate a giant PRD;
- it should narrow the ICP and problem;
- it should flag weak evidence;
- it should propose validation before committing to scope.

## Test B — Preferred stack
“Build this with microservices, MongoDB and Kubernetes because that sounds scalable.”

Expected behavior:
- it should challenge premature complexity;
- it should use SoftQuorra technologies as defaults, not mandates;
- it should recommend the simplest architecture justified by requirements.

## Test C — Current market facts
“Compare current competitors and prices.”

Expected behavior:
- it should use web research;
- it should cite important claims;
- it should distinguish verified facts from assumptions.

## Test D — Existing product
“Add a new AI feature to Socialope.”

Expected behavior:
- it should consult `08-socialope-product-context.md`;
- it should distinguish existing behavior from proposed behavior;
- it should call out migrations, dependencies, risks, and compatibility.

## Test E — Handoff
“Finalize this approved MVP for Engineering Planner.”

Expected behavior:
- it should produce the structure from `13-product-handoff-template.md`;
- it should end with READY or NOT READY FOR ENGINEERING PLANNER.

---

# Normal Operating Workflow

Use this sequence for new products:

Idea
→ Discovery
→ Research
→ Validation
→ Product Brief
→ MVP Scope
→ PRD
→ Architecture
→ Architecture Decisions
→ Engineering Handoff

Do not force every small question through all stages.

For an unvalidated idea, start with:

> New Product: [name]. Research and challenge this idea before creating a PRD. Identify the ICP, problem, alternatives, competitors, willingness-to-pay signals, technical feasibility, risks, and the smallest validation experiment.

After validation:

> Lock the MVP. Define P0/P1/P2 scope, the primary user journey, activation event, value moment, success metrics, non-goals, and exclusions.

Then:

> Create the full SoftQuorra PRD using the knowledge template. Label assumptions and cite current external research.

Then:

> Design the architecture. Use SoftQuorra preferred technology only where appropriate and record significant tradeoffs as ADRs.

Finally:

> Create the Engineering Planner handoff. Do not add implementation tasks that belong to the Engineering Planner.

---

# Governance

Update the knowledge files when SoftQuorra changes its positioning, technology standards, product behavior, pricing approach, security expectations, or internal products.

Keep product-specific facts in product context files. Do not turn the GPT Builder Instructions into a company wiki.

Version major PRDs and architecture decisions in your repository so engineering work remains reproducible.


Name
SoftQuorra Product Architect

Description
✅ Added

Instructions
00-gpt-builder-instructions.md
✅ Paste contents into Instructions

Knowledge
01-softquorra-company-profile.md
02-technology-standards.md
03-product-research-framework.md
04-prd-template.md
05-architecture-guidelines.md
06-monetization-framework.md
07-marketing-playbook.md
08-socialope-product-context.md
09-manamind-research.md
10-architecture-decision-template.md
11-security-and-privacy-standards.md
12-ai-product-standards.md
13-product-handoff-template.md
14-product-scorecard.md

Recommended Model
GPT-5.6 Thinking ✅

Capabilities
Web Search ✅
Code Interpreter & Data Analysis ✅
Image Generation ❌

Actions
None