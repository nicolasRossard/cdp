# LESSONS

## [2026-11-01] Do not commit generated trace files

**Context**: `git add -A` after "commit tout" in a fresh repo with MLflow tracing and AIAD installed.

**Error**: `mlartifacts/` (Claude session traces), `.aiad/.cache/` and `.aiad/metrics/` were committed and pushed to a public repo.

**Correction**: Check `git status` for generated/local folders and add them to `.gitignore` before committing.

**Impact**: History rewritten and force-pushed to remove the traces.
