# Bead: bob-cli-26.2 — Editor protocol, help, and documentation

[Bead Pages](../README.md) / [bob-cli-26](README.md) / bob-cli-26.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.20](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.20/README.md) · **Assignee:** `bob-cli-26.2` · **Size:** medium
**Created:** 2026-09-26 16:50:55 EDT · **Closed:** 2026-09-26 17:24:53 EDT
**Plan:** [202609/capture\_start\_pomodoro.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/capture_start_pomodoro.md)

## Description

capture-editor-contract: expose start metadata, parsing spans, completion-safe replacement ranges, and documented examples.

## Notes

[2026-09-26T21:24:39Z · bob-cli-26.2] PROPOSED FOLLOW-UP: cargo fmt --check fails repo-wide on the clean base tree (installed rustfmt 1.9.0 disagrees with committed style, e.g. src/lib.rs, dataview/, vault_sync.rs); reformat drift separately, not in a phase bead

[2026-09-26T21:24:53Z · bob-cli-26.2] Editor contract done: capture-parse reports additive pomodoro_start (raw/duration_units/offset_units) with non-overlapping pomodoro_start spans and invalid_pomodoro_start diagnostics; capture-complete name/block ranges end before = and cursor-in-suffix is empty; capture JSON/human start output verified additive (phase 1); README + docs/capture.md grammar tables, se<X> table, and parse/complete protocol documented. Verified: cargo clippy clean (1 pre-existing warning), cargo test 1437 passed 0 failed (903 lib incl 5 new unit tests, 475 cli incl 4 new protocol tests). Pre-existing repo-wide cargo fmt drift recorded as follow-up.

## Dependencies

- **Depends on:** [bob-cli-26.1](bob-cli-26.1.md) ✓ · ⧖ 2026-09-26
- **Blocks:** [bob-cli-26.3](bob-cli-26.3.md) ◐ · ⧖ 2026-09-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-26.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-26.2/README.md) | [bob-cli-26.2](bob-cli-26.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`dd47456`](https://github.com/bobs-org/bob-cli/commit/dd474564c17bccee8f652c2d54706f3a4e0a935d) | feat(capture): expose atomic-start editor contract, help, and docs | [bob-cli-26.2](bob-cli-26.2.md) | 2026-09-26 17:26:00 EDT |
