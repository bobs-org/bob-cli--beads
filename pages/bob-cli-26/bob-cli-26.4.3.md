# Bead: bob-cli-26.4.3 — Fix global plus-commit capture-complete argv

[Bead Pages](../README.md) / [bob-cli-26.4](bob-cli-26.4.md) / bob-cli-26.4.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-26.4.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-26.4.land.md) · **Assignee:** `bob-cli-26.4.3.land`
**Created:** 2026-09-26 18:20:14 EDT · **Closed:** 2026-09-26 18:57:04 EDT
**Plan:** [202609/global\_plus\_commit\_argv.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/global_plus_commit_argv.md)

## Description

Bob Mac Capture's swift test suite passes on macOS 26, including the global route plus-commit that must request task completion at cursor 12.

## Notes

[2026-09-26T22:57:04Z · bob-cli-26.4.3.land] Verified phase bob-cli-26.4.3.1 and committed Mac fixture fix 1a5f7a5: fake-bob serializes multiline argv record appends via an atomic mkdir lock and TERM/INT cleanup, preserving the existing capture-complete cursor-12 path. GitHub Actions macOS 26 run 36277377633 passed build, full 503-test suite (including global plus-commit and diagnostic-range tests), bundle, smoke, and install checks; phase also reported 20/20 focused iterations. Reviewed Mac source/commit and bob-cli history: no non-epic base-branch commits since this child epic began, and no integration changes needed. The only child note reported this fix and verification; there were no PROPOSED FOLLOW-UP entries to file or decline. No --epic-symbol entries.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-26.4.3.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-26.4.3.land/README.md) | [bob-cli-26.4.3](bob-cli-26.4.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli--plans | [`bob-cli--plans@64fcb57`](https://github.com/bobs-org/bob-cli--plans/commit/64fcb5726cf8d436cdc82fae19c5a012558d8d7f) | docs(plans): mark Pomodoro capture epics done | [bob-cli-26.4.3](bob-cli-26.4.3.md) | 2026-09-26 19:01:52 EDT |
