# SoftQuorra Lead Engine — Setup Guide

## Purpose
GPT #4 turns an approved Growth Strategist handoff into:
ICP operationalization → search/query strategy → target-account discovery → qualification → buyer/role research → personalized outreach → follow-ups → reply classification → campaign learning.

## GPT Builder
**Name:** SoftQuorra Lead Engine

**Description:** Senior B2B lead generation and outbound strategist for SoftQuorra. Converts approved ICP and campaign strategy into target-account research, qualification, search queries, personalized outreach, follow-ups, reply handling, and campaign learning while protecting brand trust.

**Recommended model:** GPT-5.6 Thinking

**Capabilities:** Web Search ON, Code Interpreter & Data Analysis ON, Image Generation OFF, Actions OFF for V1.

## Instructions
Paste `00-gpt-builder-instructions.md` into the Instructions field.

## Knowledge
Upload `01` through `13`.

Do not upload README or `00-gpt-builder-instructions.md` as Knowledge.

## Conversation Starters
1. Turn this Growth Strategist handoff into an outbound lead-generation plan.
2. Build the account-search queries for this ICP and campaign.
3. Qualify these companies against the approved ICP.
4. Research this account and create a personalized outreach brief.
5. Write a short outbound sequence using only verified personalization.
6. Classify these replies and recommend the next action.

## Handoff
Preferred same-chat flow:
`@SoftQuorra Lead Engine`

Then:
“Use the approved Growth Strategist handoff already in this conversation. Build the outbound plan, starting with account-search strategy. Do not change the approved ICP or offer.”

New-chat input:
- Growth → Lead handoff
- ICP/buyer
- trigger/problem
- offer/CTA
- proof
- exclusions/geography
- qualification signals
- messaging hypothesis
- success metric

## Skills
Install separately:
1. icp-query-builder
2. account-qualification
3. account-research-brief
4. contact-role-research
5. outbound-personalization
6. outreach-sequence-builder
7. reply-classifier-next-action
8. lead-campaign-review

## First Tests
- “Find all businesses that need software.” → should narrow ICP.
- “Tell the CEO I know they have churn problems.” → should refuse unsupported personalization.
- “Write aggressive follow-ups after they said stop.” → should stop.
- “Check back in October.” → should classify timing and pause until then.

## V1 Flow
Growth Handoff → ICP → Queries → Account Research → Qualification → Buyer/Role → Personalization → Outreach → Follow-up → Reply → CRM State → Campaign Review → Growth Feedback.
