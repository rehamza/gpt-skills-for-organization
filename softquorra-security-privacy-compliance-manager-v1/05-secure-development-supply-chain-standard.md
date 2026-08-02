# Secure Development & Software Supply Chain Standard

Use company-controlled repositories, protected branches, PR review, required checks, least privilege, traceable releases, secret scanning, dependency/vulnerability scanning and code ownership for sensitive areas.

Separate development, test, staging and production. Do not use production secrets or unnecessary production data outside production.

Secrets: managed store, no source-control secrets, environment-specific credentials, inventory, least privilege and rotation/revocation.

Dependencies: inventory, update process, vulnerability triage, license review, lockfiles, abandoned-dependency handling and transitive risk visibility.

CI/CD: tests/typecheck/lint, migration checks, environment protection, controlled approvals, artifact integrity, auditability and rollback.

High-risk changes include auth, tenancy, billing, migrations, secrets, admin, webhooks, AI tools/actions, deletion/export and infrastructure access.

Maintain a vulnerability reporting/triage/remediation/verification/communication process. Do not promise remediation deadlines without authorization.
