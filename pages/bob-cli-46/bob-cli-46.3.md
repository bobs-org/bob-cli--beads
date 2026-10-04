# Bead: bob-cli-46.3 — README, docs, and tests teach the canonical names

[Bead Pages](../README.md) / [bob-cli-46](README.md) / bob-cli-46.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.4y](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.4y.md) · **Assignee:** `bob-cli-46.3` · **Size:** medium
**Created:** 2026-10-04 07:02:06 EDT · **Closed:** 2026-10-04 09:23:49 EDT
**Plan:** [202610/bob\_command\_tree.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_command_tree.md)

## Description

canonical-docs: rewrite the README command reference, task and Pomodoro sections, shims table, and migration notes; move docs/ to canonical spellings; migrate test invocations to canonical paths; and record the proposed follow-ups.

## Notes

[2026-10-04T13:22:49Z · bob-cli-46.3] PROPOSED FOLLOW-UP: vault_sync::run_notify missing PRE/POST sleeps — src/native/vault_sync.rs still runs `bob notify` with no PRE_CHECK_SLEEP/POST_NOTIFY_SLEEP, so conflict notification always fails with a usage error and never notifies. Canonical path is `bob pomodoro notify`; argv left unchanged in this phase per plan.

[2026-10-04T13:22:54Z · bob-cli-46.3] PROPOSED FOLLOW-UP: unify -j/--json with -f/--format json — feature (R8): some commands take -j/--json and others take -f/--format json; unify them across the tree.

[2026-10-04T13:23:02Z · bob-cli-46.3] PROPOSED FOLLOW-UP: normalize singular/plural command nouns — feature (R8): `projects` and `plugins` are plural while `task` is singular; pick one noun policy.

[2026-10-04T13:23:07Z · bob-cli-46.3] PROPOSED FOLLOW-UP: restyle hand-parsed help — feature (R8): restyle the hand-parsed help for `nightly`, `pomodoro status|tmux|notify`, and `task archive` to match clap-rendered help.

[2026-10-04T13:23:12Z · bob-cli-46.3] PROPOSED FOLLOW-UP: decisions record for command-tree policy — memory: propose a decisions record covering sectioned help over nesting, the narrow `bob task` rule, permanent silent aliases, and the frozen `capture-*` protocol; name the rejected options (a broad `bob task`, `capture-api`, `bob vault`, deprecation hints) and cite research:202610/bob_cli_command_tree_reorganization.

[2026-10-04T13:23:44Z · bob-cli-46.3] PROPOSED FOLLOW-UP: clippy deny overly_complex_bool_expr at tests/cli/capture/pomodoro_name.rs:808 (`|| true`) — reproduces on the clean base tree (git blame 22abed4, bob-cli-28.1). Owned by in-progress epic bob-cli-28 closeout; no separate task bead. Does not keep this phase open.

[2026-10-04T13:23:49Z · bob-cli-46.3] README, docs, and tests now teach canonical names. README: 14-row sectioned commands table, Task maintenance (reconcile/reroll/archive), Pomodoro, shims, and old→canonical migration notes. docs/ keep filenames with at most one formerly note; crontab uses bob task reconcile; freshness seed stays hidden. Tests invoke canonical paths (task reconcile/archive/reroll, pomodoro tmux/notify); aliases.rs, renamed_old_top_level, justfile install-smoke old --help, protocol.rs typed-alias completion, and vault_sync renamed_old stay as alias/parity coverage. Residual rg leftovers are alias tables, persisted recovery id task-status-hooks, internal module/file names, vault_sync::run_notify, historical narrative, or a single formerly note. Five plan follow-ups recorded as PROPOSED FOLLOW-UP notes. cargo fmt clean; cargo test --test cli --test randomize: 948 + 15 passed. sase bead epic-symbols: no leftovers.

[2026-10-04T13:34:20Z · bob-cli-46.3--2] just all failed only on clippy overly_complex_bool_expr at tests/cli/capture/pomodoro_name.rs:808 (`|| true`); reproduces on the clean base tree (bob-cli-28). Canonical-docs work is otherwise complete; committing with bead_action close.

## Dependencies

- **Depends on:** [bob-cli-46.2](bob-cli-46.2.md) ✓ · ⧖ 2026-10-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-46.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-46.3.md) | [bob-cli-46.3](bob-cli-46.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`192e8b5`](https://github.com/bobs-org/bob-cli/commit/192e8b51157a7616ddeecf4161667b0c538699e6) | docs(cli): teach canonical task and pomodoro names | [bob-cli-46.3](bob-cli-46.3.md) | 2026-10-04 09:35:22 EDT |
