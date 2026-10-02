# Bead: bob-cli-3j.1 — One composed clap command tree for completion

[Bead Pages](../README.md) / [bob-cli-3j](README.md) / bob-cli-3j.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.46](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.46.md) · **Assignee:** `bob-cli-3j.1` · **Size:** medium
**Created:** 2026-10-02 11:06:15 EDT · **Closed:** 2026-10-02 11:24:19 EDT
**Plan:** [202610/bob\_shell\_completion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_shell_completion.md)

## Description

one-tree: build an exhaustive, completion-only clap tree from the module builders plus descriptors for the five hand-parsed commands and the bare default-subcommand forms, guarded by parity, parse-smoke, and help-drift tests, with no user-visible change.

## Notes

[2026-10-02T15:24:08Z · bob-cli-3j.1] PROPOSED FOLLOW-UP: fix pre-existing clippy deny overly_complex_bool_expr at tests/cli/capture/pomodoro_name.rs:808 (|| true) — reproduces identically on clean base tree (cargo clippy exit 101), unrelated to one-tree changes

[2026-10-02T15:24:19Z · bob-cli-3j.1] one-tree done: completion-only clap tree over all 27 SUBCOMMANDS plus hand-parser descriptors and bare freshness/vault-sync forms; tree tests (parity/order/no-space/no-help/debug_assert/9 parse smokes/drift) pass, cargo fmt clean, full cargo test green incl 56 help tests; just lint fails only on pre-existing tests/cli/capture/pomodoro_name.rs:808 clippy deny verified identical on clean base (recorded as follow-up)

## Dependencies

- **Blocks:** [bob-cli-3j.2](bob-cli-3j.2.md) ◐ · ⧖ 2026-10-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-3j.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-3j.1/README.md) | [bob-cli-3j.1](bob-cli-3j.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`71d57da`](https://github.com/bobs-org/bob-cli/commit/71d57da42a940afaa6c3fe26fb4c59cbe5b82c5c) | feat(completion): land one-tree composed clap command tree for completion | [bob-cli-3j.1](bob-cli-3j.1.md) | 2026-10-02 11:26:18 EDT |
