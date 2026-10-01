# oppia/oppia context
> refreshed 2026-10-01 | upstream default: develop @ 1f36809d9dc79a1bf74f1e0dc4d7f78a8a6e73f8

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
- `2026-09-24` issue #27488 (whitespace-only TextInput reply submitted+classified instead of no-response) - outcome pr-opened (https://github.com/olitreadwell/oppia/pull/32) - lesson: real backend-logic bug from an open unclaimed upstream issue; submitAnswer guard + StateCard.showNoResponseError both treated only '' as no response. Fixed + spec cases added; locally-verified via node before/after repro + TS parse + prettier (oppia full suite needs oppia_tools, not feasible here; fork CI not connected).
- `2026-09-03` self-found gap (trivial pass) - outcome pr-opened (https://github.com/olitreadwell/oppia/pull/1) - lesson: en.json/UI strings clean; genuine typos live in comments/docstrings; oppia CI not connected to forks so fork shows no runs.
- `2026-09-30` fork-hygiene - outcome closed (https://github.com/olitreadwell/oppia/pull/1 and https://github.com/olitreadwell/oppia/pull/12) - lesson: an in-place squash force-push made oppia's own `.github/workflows/close_pr_on_force_push.yml` close both PRs within a minute. NEVER force-push (or rebase) an oppia PR branch; re-stage consolidated work on a fresh branch off develop instead. After that, both PRs were closed and no open fork PR represented the fixes.
- `2026-10-01` self-found gap (trivial pass #4) - outcome pr-opened (https://github.com/olitreadwell/oppia/pull/39) - lesson: re-staged the lost typo/doc/link fixes on a FRESH branch `fix-typos-in-comments-and-ui-text` (new commit, no force-push) and added fresh, previously-unreported typos; 28 corrections across 10 files, +23/-23. Note: fork CI now creates check runs (queued) rather than none, but every job sits queued and never starts on the fork (all workflows, incl. ubuntu-latest ones), so local verification (prettier + py_compile + live 404/200 link checks) is the only signal available.

## Mined gaps
- none yet — this run does a trivial-fix pass (typos/dead links/stale commands) per engine/loop-trivial.sh.
- `2026-09-09` self-found gap (trivial pass #2) - outcome pr-opened (https://github.com/olitreadwell/oppia/pull/11) - lesson: second typo pass found 31 more genuine misspellings across 10 files (comments/docstrings/error messages); en.json/UI strings still clean; oppia CI not connected to forks so fork shows no runs.
- `2026-09-09` self-found gap (trivial pass #3) - outcome pr-opened (https://github.com/olitreadwell/oppia/pull/12) - lesson: dead links (pencilcode.html, ossf secure-sw-dev-fundamentals, drive video) verified 404 + typos in comments/docstrings/test descriptions across 10 files; oppia CI not connected to forks so fork shows no runs.
