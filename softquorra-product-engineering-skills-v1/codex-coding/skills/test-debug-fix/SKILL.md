---
name: test-debug-fix
description: Diagnoses failing tests, runtime bugs, regressions, type/lint/build failures, or incorrect behavior and applies the smallest root-cause fix with regression coverage. Use when tests fail, a bug report exists, or an implementation needs debugging.
metadata:
  author: softquorra
  version: "1.0"
---

# Test Debug Fix

## Goal
Fix the root cause while preserving approved product behavior and preventing regression.

## Workflow
1. Reproduce the failure using the narrowest reliable command/path.
2. Capture expected vs actual behavior and inspect related code/tests/logs.
3. Classify root cause: product mismatch, implementation bug, test bug, environment/config issue, data/migration issue, or external provider issue.
4. Implement the smallest correct fix.
5. Add/update regression coverage that would fail before the fix.
6. Run focused validation, then broader affected checks.
7. Review for collateral changes and report root cause, fix, evidence, and remaining risk.

## Output
- Reproduction
- Root cause
- Fix
- Regression test
- Commands/results
- Remaining risk

## Quality / Guardrails
- Do not delete/weaken a valid test just to pass.
- Do not silently change approved behavior to match buggy code.
