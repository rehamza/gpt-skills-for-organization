# Socialope Product Context

## Status

Pre-launch. Socialope (a SoftQuorra product) is **not yet generally launched** — it is currently
in active development: ongoing product improvements, bug fixes, and social-platform connectivity
work (individual platform integrations going through their own registration/review process before
they can be relied on in production).

- **Marketing/waitlist site**: already public today, running an early-access program with
  locked-in launch pricing ahead of general availability.
- **Target launch**: early September 2026 — matches the site's own configured launch date
  (2026-09-01), used for the early-access countdown and pricing.
- **Known open item**: several social platform integrations still require registration/approval
  before they're production-ready (for example, LinkedIn's Community Management API scopes are
  still pending approval in that platform's developer portal) — "social connectivity" issues are
  an active, tracked work item, not a finished capability.

Re-confirm this status before using this document for any external-facing decision — launch
timing and outstanding platform approvals can change as the work progresses.

## Product Positioning

Socialope is an AI-first marketing/growth workspace that connects content creation, social
publishing, audience engagement, lead discovery/qualification, and outreach in one product,
instead of the usual stack of a separate scheduler, inbox tool, prospecting tool, and cold-email
tool.

The product's defining mechanic is a roster of specialized AI agents that draft the work — posts,
replies, lead lists, lead scores, outreach sequences — while a human keeps final approval over what
actually ships, unless a workspace deliberately turns that autonomy up.

## Publicly Presented Target Users

Broad public segments referenced across the marketing site and use-case library:

- Founders and solopreneurs building a personal brand or promoting an early-stage product/MVP.
- Small marketing teams and B2B/SaaS companies running content and outreach together.
- Agencies managing social presence and/or outreach for multiple client brands from one account.
- Local/service businesses — restaurants and cafes, medical/dental clinics, fitness studios,
  real estate agents, beauty/salon businesses, nonprofits.
- E-commerce brands, recruiting/staffing agencies, consultants, and B2B sales teams doing cold
  outreach.

These are broad public segments, each backed by a dedicated use-case page. For a specific feature
or campaign decision, narrow to the actual ICP rather than treating this list as one audience.

## Current Public Product Promise

Core message (from the site's own copy): *"Meet your AI growth team. Agents handle the drafting,
replying, and follow-up busywork. You decide what ships — and where the pipeline goes."*

Restated: reduce the fragmented workflow across a scheduler, a social inbox, a lead-discovery
tool, a lead-scoring process, and an outreach tool, by having AI agents do the repetitive
drafting/research work inside one workspace, with a human approval step as the connective tissue
between all of it.

## Public Workflow

The current public product communicates a six-step journey, each step owned by a specific agent
or platform surface:

1. **Create** — Content Agent turns one source into a platform-native draft.
2. **Publish** — the queue and calendar ship it to the connected platforms on schedule.
3. **Engage** — Engagement Agent replies to comments before they go cold.
4. **Discover** — Lead Finder searches the web for companies matching the ideal customer profile.
5. **Qualify** — Lead Qualifier scores and sorts every lead by fit, automatically.
6. **Follow up** — Campaign Agent turns the qualified lead list into a running outreach sequence.

## AI Agent Concepts Currently Presented

### Content Agent

Creates platform-native content drafts from sources such as a website, RSS feeds, competitor
social accounts, news topics, or keywords, and publishes approved drafts on a schedule. Public
framing: roughly 8 platform-ready drafts a week land in the approval queue by default.

### Engagement Agent

Monitors comments and mentions across every connected platform and drafts an on-brand reply for
each one, typically within minutes of a new comment.

### Lead Finder

Given a description of the ideal customer (ICP), searches the web for real, matching companies
and saves them into a new lead list automatically — publicly framed as up to 200 new leads a
month. It only researches and saves; it never sends anything or contacts anyone itself.

### Lead Qualifier

Scores every lead in an existing list — Hot, Warm, or Cold — against the same ICP, with a
plain-English reason for the score, and re-sorts the list as new leads are added. Read-only: it
never removes or contacts a lead.

### Campaign Agent

Reads a lead list and an objective and drafts a complete multi-step outreach sequence (emails,
wait steps, follow-ups) ready for review before anything sends.

## Human Approval Principle

A central current product principle is approval-first behavior: AI agents prepare work and a
human decides what ships. This is implemented today as four selectable autonomy levels, settable
per agent:

- **Draft-only** — a human always writes/edits the final version themselves.
- **Approve-first** (default) — the agent's draft waits in a shared approval queue.
- **Auto-schedule** — an approved draft goes straight onto the calendar with no extra click.
- **Auto-publish** — the agent's work goes out on its own within the limits set for it.

Two permanent exceptions sit outside the plan/autonomy setting entirely and should be treated as
fixed product guarantees, not configurable behavior:

- **Campaign Agent's outbound email is always approval-first**, regardless of autonomy level or
  plan — this is a hardcoded compliance guarantee, not a default that can be turned off.
- **Lead Finder and Lead Qualifier never need approval at all** — they only research and score;
  there is nothing for a human to approve until their output is used elsewhere.

Any proposal to increase autonomy anywhere in the product must explicitly define:

- autonomy level;
- approval boundary (what specifically bypasses human review, and what never can);
- rollback/cancel path;
- who has permission to change it;
- audit trail (a workspace-level audit log already exists and should be extended, not
  reinvented, for any new autonomy-affecting action);
- rate/spend limits (existing precedent: per-day publish caps, per-month AI-action and lead
  quotas, purchasable overflow credits);
- failure behavior (existing precedent: agents degrade to draft/escalate rather than fail silently
  or retry indefinitely).

## Publishing / Workspace Context

Public product material describes:

- a content composer with single- and multi-destination AI variant generation;
- platform-specific variants (length, formatting) generated from one draft;
- exact publishing-target selection (a specific page, profile, group, channel, or board — not just
  "the account");
- a queue/calendar with draft, scheduled, published, and failed states;
- media library and idea capture;
- comments/inbox kept attached to the post they belong to, not siloed per platform;
- per-platform analytics.

The public site currently markets eight platforms: Instagram, TikTok, LinkedIn, X, Facebook,
YouTube, Threads, and Pinterest. Note for verification: the product's actual connected-platform
support in code is broader than the eight publicly marketed platforms (for example, Bluesky
publishing and comment-sync exist in the codebase but are not part of the current public
marketing list) — treat the public platform list as a marketing subset, not a ceiling, and
re-verify current code before assuming a platform is or isn't supported.

Exact integration capabilities, API permissions, and production implementation must be verified
from current internal code/docs and each platform's own developer documentation before
architectural decisions — platform API policies change independently of this product.

## Outreach Context

Public product material describes:

- a visual, graph-based sequence builder (emails, wait steps, goals);
- contacts and lead lists, including CSV import;
- sender setup across multiple providers (Gmail, Outlook, Zoho, Yahoo, Resend, custom SMTP) with
  sender health monitoring (deliverability signals, bounce/complaint-rate thresholds);
- automatic reply detection and classification (genuine reply, bounce, out-of-office,
  unsubscribe), with a sequence stopping automatically once a contact replies;
- pipeline stages from first touch to booked meeting;
- campaign-level analytics and reporting;
- a library of ready-made sequence templates (a small free "starter" set plus a larger
  "premium" set gated to paid plans), shared across a workspace rather than owned by one agent or
  one user, with "duplicate to customize" as the only path to an editable copy of a shared
  template.

Do not assume every publicly described capability has identical production behavior. Confirm
implementation when a feature decision depends on it — this product has a working history of
public/marketing framing and backend implementation drifting apart on specific details (plan
limits, included quotas, and credit/quota pooling models have all been revised at least once).

## Product Architecture Guidance

When proposing Socialope changes:

1. preserve the unified workspace concept (content + outreach sharing one account, one agent
   roster, one approval queue) unless evidence supports a strategy change;
2. preserve approval-first safety for consequential agent actions unless explicitly redesigned,
   and never weaken Campaign Agent's always-approval-first outbound-email guarantee;
3. avoid duplicating existing content/lead/campaign concepts — check which module already owns a
   concept (Publish, Outreach, Agents, or Billing) before introducing a parallel one;
4. identify which existing domain owns the feature before building in a new one;
5. document migration and compatibility, especially for any schema or plan-entitlement change;
6. evaluate platform/API limits (rate limits, scopes, policy changes) before committing to a
   platform-dependent feature;
7. evaluate AI/API variable cost (model tier, token volume, per-action pricing) before shipping a
   new AI-driven action, and meter it consistently with the existing AI-action/lead-credit system
   rather than inventing a new metering mechanism;
8. protect tenant/workspace data boundaries — this is a multi-tenant product; every query and
   permission check must be scoped to the acting workspace;
9. instrument agent success/failure and approval outcomes so a feature's real-world performance
   (not just its existence) is observable after launch.

## Change Proposal Format

For every material Socialope feature change:

### Existing Behavior

What the product currently does, based on internal context/code or verified public behavior.

### Proposed Behavior

What changes.

### User Value

Which user/problem improves.

### Scope

P0/P1/P2.

### Data Changes

Entities/fields/migrations.

### Integration Changes

New scopes, APIs, webhooks, rate limits.

### AI Changes

Prompts/models/tools/evals/approval.

### Compatibility

Backward compatibility, migrations, existing workflows.

### Metrics

Activation/usage/quality/business result.

### Risk

Security, platform, deliverability, AI, spam/abuse, cost, UX.

## Source Maintenance Note

This file is a baseline product context. Update it from internal product documentation and
repository decisions whenever a phase of work materially changes product behavior, pricing,
autonomy rules, or platform support. Public marketing copy and platform support can change
independently of this document — verify current facts in the actual codebase/docs before relying
on any specific number, limit, or capability claim here for an architectural decision.

## Legal Owner and Operator

Product: **Socialope**

Legal owner/operator: **SoftQuorra LLC**

Socialope is a SoftQuorra LLC product and is not treated as a separate legal entity unless formally established later.

## Data Areas Requiring Review

Account/auth, billing, social tokens/data, customer content, publishing/scheduling, engagement/replies, leads/contacts, campaigns/outreach, AI prompts/outputs, analytics/logs, support and vendors.

Controller/processor status is assessed per processing activity and jurisdiction.

## Trust/Governance Artifacts

Assess Terms, Privacy Policy, Cookie Notice, AUP, DPA, Subprocessor List, Security Overview, retention/deletion, incident process, rights requests, billing terms, vendor reviews, threat models and release evidence.

Do not claim certification/compliance without current authorized evidence.
