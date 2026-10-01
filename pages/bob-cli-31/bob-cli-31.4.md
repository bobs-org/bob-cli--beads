# Bead: bob-cli-31.4 — Seed the live vault and mute the fields

[Bead Pages](../README.md) / [bob-cli-31](README.md) / bob-cli-31.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.v.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.v.linker.w0.md) · **Assignee:** `bob-cli-31.4` · **Size:** small
**Created:** 2026-09-30 19:32:05 EDT · **Closed:** 2026-09-30 21:55:29 EDT
**Plan:** [202609/task\_freshness\_review.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/task_freshness_review.md)

## Description

seed: install bob from master, dry-run then apply bob freshness seed to ~/bob, verify that no task parses differently before and after, add the CSS rule that mutes fresh and refresh, and vault-sync.

## Notes

[2026-10-01T01:55:03Z · bob-cli-31.4] PROPOSED FOLLOW-UP: just all red on clean base - clippy overly_complex_bool_expr at tests/cli/capture/pomodoro_name.rs:808 (|| true) and 5 capture_pomodoro_close linked_task_tests failures, both reproduce on untouched master

[2026-10-01T01:55:11Z · bob-cli-31.4] PROPOSED FOLLOW-UP: mirror placement P18 blockquote-prefix stripping in bob-ledger-tools api.freshness.stampLine for bead bob-cli-31.5

[2026-10-01T01:55:29Z · bob-cli-31.4] Seed applied to ~/bob: 177 ready + 363 other across 46 files (commit 61b0921e, merge kept all 540 stamps); 540/540 changed lines differ only by [fresh::] + canonical spacing; freshness list shows new=0 due=0 refreshed_today=387; CSS mute rule for fresh/refresh added to dataview-properties.css; vault-sync clean. Fixed stamper blockquote blindness (task_status/scan_floor strip > prefixes, P18 vector+tests); fmt ok, all 52+22 freshness tests pass; clippy error and 5 capture_pomodoro_close failures reproduce on clean base (recorded as follow-ups).

## Dependencies

- **Depends on:** [bob-cli-31.2](bob-cli-31.2.md) ✓ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-31.5](bob-cli-31.5.md) ✓ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-31.9](bob-cli-31.9.md) ◐ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-31.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-31.4/README.md) | [bob-cli-31.4](bob-cli-31.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`66c4e4c`](https://github.com/bobs-org/bob-cli/commit/66c4e4cb827abf096543e22b060d025b6f2cdc69) | feat(freshness): stamp blockquoted tasks, seed live vault cutover (bob-cli-31.4) | [bob-cli-31.4](bob-cli-31.4.md) | 2026-09-30 21:59:55 EDT |
