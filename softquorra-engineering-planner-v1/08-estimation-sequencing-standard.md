# SoftQuorra Estimation & Sequencing Standard

## Principle
Estimate to support decisions and sequencing, not to create false certainty.

Unknown requirements produce uncertain estimates.

# 1. Size After Decomposition
Do not estimate a whole MVP before scope, dependencies, architecture, repo context, major integrations, and important unknowns are understood enough.

# 2. Relative Sizing
Suggested:
- XS — trivial/localized;
- S — small bounded change;
- M — moderate change across a few components;
- L — large/cross-cutting;
- XL — too large; decompose or spike.

# 3. Time Ranges
When time estimates are requested, use ranges with team assumptions, review/testing, integration lead time, and uncertainty.

Example: `3–5 engineering days assuming existing auth and schema patterns are available.`

Do not promise exact dates from incomplete inputs.

# 4. Uncertainty
Identify product, technical, external/provider, migration/data, and QA/security uncertainty.

Use a spike when uncertainty dominates.

# 5. Dependency Types
- Hard prerequisite
- Soft prerequisite
- External/provider
- Decision
- Data/migration

# 6. Critical Path
Pay special attention to provider approvals, schema foundations, auth/tenancy, risky migrations, uncertain AI/API capabilities, and release dependencies.

# 7. Vertical Slices
Prefer foundation only when required → thin end-to-end behavior → expand → harden → rollout.

A slice should be demoable/verifiable.

Avoid sequencing the whole project as backend → frontend → testing unless requirements truly demand it.

# 8. Parallelization
Potential tracks include frontend using an agreed mocked contract, backend/data, integration spike, AI eval/prompt work, infrastructure, and QA preparation.

Parallelize only after shared contracts are clear enough to avoid rework.

# 9. Sequencing Output
For each slice provide objective, requirements, prerequisites, tasks, parallel tasks, demo/verification, risks, and estimate/range if requested.

# 10. Planning Reserve
Do not hide uncertainty in padding. State implementation range, uncertainty driver, contingency, and the decision/spike that can reduce uncertainty.
