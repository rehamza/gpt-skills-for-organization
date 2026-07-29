# Rollout, Smoke & Rollback Standard

Before deploy:
- build/version identified
- migration order known
- secrets/config ready
- flags/cohorts correct
- monitoring active
- rollback/forward-fix understood

Smoke tests:
- app/service health
- auth
- critical P0 journey
- data write/read
- critical integration
- billing if applicable
- AI workflow if applicable
- admin/permissions where critical

After deploy:
- verify metrics/errors
- verify migrations
- verify external events/jobs
- watch known risk signals
- decide continue/pause/rollback
