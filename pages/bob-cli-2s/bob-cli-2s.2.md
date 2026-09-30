# Bead: bob-cli-2s.2 — bob-cli: \`=\[\<X\>\]\[#name\]~\<K\>\` grammar, editor support, and docs

[Bead Pages](../README.md) / [bob-cli-2s](README.md) / bob-cli-2s.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3f](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3f.md) · **Assignee:** `bob-cli-2s.2` · **Size:** medium
**Created:** 2026-09-30 08:28:32 EDT · **Closed:** 2026-09-30 09:45:05 EDT
**Plan:** [202609/start\_drop\_queued\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/start_drop_queued_links.md)

## Description

start-drop-grammar: lex the trailing `~<K>` drop list on whole-item starts. Wire it through `bob capture` (execution, batches, chains) into the start-lineup engine. Mirror it in `capture-parse` (the `pomodoro_start_drop` span, the `pomodoro_start_task` need, incomplete states, precise diagnostics) and in `capture-complete`. Document the gesture everywhere.

## Notes

[2026-09-30T13:38:08Z · bob-cli-2s.2] PROPOSED FOLLOW-UP: cargo clippy --all-targets fails on the clean base tree in tests/cli/capture/pomodoro_name.rs:808 (overly_complex_bool_expr from `|| true`); pre-existing, unrelated to the start-drop grammar

[2026-09-30T13:45:05Z · bob-cli-2s.2] Closed by explicit `sase stitch create -B close` after create_commit landed 1121e06 ("feat(capture): start-drop grammar for whole-item starts"). The commit author requested bead completion after verifying the bead scope. Reopen with `sase bead open bob-cli-2s.2` if more work remains.

## Dependencies

- **Depends on:** [bob-cli-2s.1](bob-cli-2s.1.md) ✓ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-2s.3](bob-cli-2s.3.md) ✓ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2s.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2s.2/README.md) | [bob-cli-2s.2](bob-cli-2s.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1121e06`](https://github.com/bobs-org/bob-cli/commit/1121e06d77f6e8a18a771b4a1b172e36ff7bed83) | feat(capture): start-drop grammar for whole-item starts | [bob-cli-2s.2](bob-cli-2s.2.md) | 2026-09-30 09:44:41 EDT |
