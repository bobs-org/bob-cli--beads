# Bead: bob-cli-46.1 — Sectioned help, help routing, and completion parity

[Bead Pages](../README.md) / [bob-cli-46](README.md) / bob-cli-46.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.4y](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.4y.md) · **Assignee:** `bob-cli-46.1` · **Size:** medium
**Created:** 2026-10-04 07:02:05 EDT · **Closed:** 2026-10-04 07:37:27 EDT
**Plan:** [202610/bob\_command\_tree.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_command_tree.md)

## Description

sectioned-help: replace CompletionTier with workflow Sections, render sectioned root help (-h collapses the capture protocol, --help lists it), cut the examples, add the argv alias-rewrite table and `bob help <path>` routing, hide `freshness seed`, label defaults, group `bob <TAB>` by section, and amend cli_rules.md. No command changes behavior.

## Notes

[2026-10-04T11:37:08Z · bob-cli-46.1] PROPOSED FOLLOW-UP: Fix the pre-existing clippy::overly_complex_bool_expr deny at tests/cli/capture/pomodoro_name.rs:808-811 — cargo clippy --all-targets --all-features fails identically on clean base HEAD fc438bc; the active owner is epic bob-cli-28, and no matching task bead exists.

[2026-10-04T11:37:27Z · bob-cli-46.1] Verified sectioned help/completion parity, alias and help routing, hidden freshness seed, default labels, and help snapshots. just test passed (1638 unit tests, 936 CLI tests, and remaining integration suites); just install-smoke passed. just all stops at the pre-existing clippy deny in tests/cli/capture/pomodoro_name.rs:808-811, reproduced on clean base HEAD fc438bc and recorded as a PROPOSED FOLLOW-UP owned by bob-cli-28.

## Dependencies

- **Blocks:** [bob-cli-46.2](bob-cli-46.2.md) ✓ · ⧖ 2026-10-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-46.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-46.1/README.md) | [bob-cli-46.1](bob-cli-46.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`660c171`](https://github.com/bobs-org/bob-cli/commit/660c171c6b281053d86907b3e908fce032f8f141) | feat(cli): add sectioned help and routing | [bob-cli-46.1](bob-cli-46.1.md) | 2026-10-04 07:44:26 EDT |
