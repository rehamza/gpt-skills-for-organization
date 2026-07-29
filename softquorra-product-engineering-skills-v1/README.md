# SoftQuorra Product & Engineering Skills V1

This library contains portable Skills for:

- Product Architect
- Engineering Planner
- Codex / VS Code coding work

## Operating Model

GPT = organizational role and judgment

Skill = reusable SOP/workflow

Project documents = current product state

Codex = repository implementation

QA & Release Manager = final verification/release role

## End-to-End Flow

Idea / existing-product change
→ Product Architect GPT
→ Product Architect Skills
→ PRD + Engineering Handoff
→ Engineering Planner GPT
→ Engineering Planner Skills
→ CODEX work packages
→ Codex / VS Code
→ Codex Coding Skills
→ Implementation Completion Report
→ QA & Release Manager

## Automatic Skill Selection

When a Skill is installed and available, ChatGPT can automatically use a relevant Skill based on the task and the Skill's description. You can also explicitly select/mention a Skill where supported.

Keep descriptions narrow and specific to prevent the wrong Skill from activating.

## ChatGPT vs Codex

Use this directory as the source of truth.

A Skill installed in ChatGPT should not be assumed to automatically appear in Codex. Install or make the same portable Skill available separately in each supported surface.

## GitHub Source of Truth

Recommended:

softquorra-product-os/
  skills/
    product-architect/
    engineering-planner/
    codex-coding/

Version Skill changes through Git so workflow changes are reviewable.
