# GPT Skills for Organization

Reusable GPT Skills, Codex Skills, and AI organization operating documents for building a practical multi-agent business workflow.

This public repository packages the SoftQuorra AI organization system: a role-based collection of Custom GPT instructions, knowledge files, repeatable SOPs, and agent skills for product strategy, engineering planning, growth, lead generation, QA release management, and coding with Codex.

## What This Repository Helps You Build

Use this repository to design, document, and operate an AI-powered organization where each assistant has a focused responsibility and a clean handoff contract.

The system is useful for:

- ChatGPT Custom GPT setup and knowledge-base packaging
- OpenAI Codex skill libraries for coding workflows
- AI agent operating systems for product and engineering teams
- Product discovery, PRDs, architecture decisions, and engineering handoffs
- Growth strategy, SEO planning, campaign briefs, and lead generation workflows
- QA planning, regression risk analysis, release readiness, and post-release checks

## Included Skill Systems

| Directory | Purpose |
| --- | --- |
| `softquorra-product-architect-v1/` | Product discovery, market research, PRDs, architecture decisions, monetization strategy, and engineering handoffs. |
| `softquorra-engineering-planner-v1/` | Approved PRD intake, implementation plans, epics, stories, technical sequencing, and Codex-ready work packages. |
| `softquorra-product-engineering-skills-v1/` | Portable Codex coding skills for repository intake, implementation, tests, debugging, API work, frontend work, migrations, integrations, and completion reports. |
| `softquorra-growth-strategist-v1/` | Positioning, GTM planning, SEO content strategy, campaign briefs, paid experiments, funnel metrics, and growth reporting. |
| `softquorra-lead-engine-v1/` | ICP targeting, account qualification, buyer research, outbound personalization, email sequences, reply handling, and campaign learning. |
| `softquorra-qa-release-manager-v1/` | Test planning, requirement traceability, regression analysis, bug triage, release readiness, smoke checks, and rollback planning. |

## Operating Model

The repository is organized around a simple AI team workflow:

```text
Product Architect
-> Engineering Planner
-> Codex / Coding Skills
-> QA & Release Manager
-> Growth Strategist
-> Lead Engine
```

Each GPT owns judgment for a specific business function. Each Skill captures a reusable workflow that can be installed, versioned, reviewed, and improved over time.

## How To Use

1. Open the setup guide for the role you want to create.
2. Paste the role's `00-gpt-builder-instructions.md` into the GPT Builder Instructions field.
3. Upload the listed numbered knowledge files for that role.
4. Install optional Skills from the role's `skills/` folder where supported.
5. Use the handoff templates to move work between roles without losing context.

For Codex, start with:

- `softquorra-product-engineering-skills-v1/codex-coding/README.md`
- `softquorra-product-engineering-skills-v1/codex-coding/skills/`

## SEO Keywords

GPT skills, Codex skills, OpenAI Codex skills, ChatGPT custom GPT instructions, AI organization, AI agents for business, agent skills, multi-agent workflow, product architect GPT, engineering planner GPT, growth strategist GPT, lead generation GPT, QA release manager GPT, prompt engineering templates, AI SOPs, PRD templates, software engineering workflow automation.

## Repository Status

This is a V1 public knowledge base for SoftQuorra's AI organization workflow. Treat the files as reusable templates and operating standards that can be adapted to your own company, product team, or AI agent stack.

## License

MIT License. See `LICENSE` for details.
