# oppia/oppia context
> refreshed 2026-09-03 | upstream default: develop @ 6279919eb7fefe072c76207b4d725baeb57cf1be

## Identity & policies
- upstream: oppia/oppia, default branch develop, primary lang Python + Angular/TS, English-first (yes — docs, wiki, issues all English).
- CLA/DCO: none required (vetted passport 2026-08-24, cla_required false).
- AI-assisted PR policy: unstated / not banned (bans_ai false).
- signed commits required: no.
- PR template: .github/PULL_REQUEST_TEMPLATE.md (fill verbatim; issue-number + Essential Checklist + PR Pointers).
- external tracker: github.

## Conventions (verified from merged PRs)
- branch naming: `fix-<desc>` or `fix-<issue>-<kebab-description>` (e.g. fix-16309-remove-webpack-infra, fix-add-tabs-contributor-admin).
- Commit/test/lint: backend `python -m scripts.run_backend_tests --test_target <path>`; lint `python -m scripts.linters.run_lint_checks` + `npx prettier --check .` (see AGENTS.md).
- CI gates merge; very high outside-merge throughput (167 external merges / 60d in queue build).
- Outside PRs merge frequently; multiple CONTRIBUTOR/COLLABORATOR PRs merge daily.

## Maintainer picture
- Active maintainers + heavy contributor swarm; response fast (recent PRs merge within days).

## Issue-area health
- Healthy. Big clean-up campaigns (style-tag cleanup parts) ongoing — avoid those specific areas.

## Gap ledger
- `2026-09-03` self-found gap (trivial pass) - outcome pr-opened (https://github.com/olitreadwell/oppia/pull/1) - lesson: en.json/UI strings clean; genuine typos live in comments/docstrings; oppia CI not connected to forks so fork shows no runs.

## Mined gaps
- none yet — this run does a trivial-fix pass (typos/dead links/stale commands) per engine/loop-trivial.sh.
