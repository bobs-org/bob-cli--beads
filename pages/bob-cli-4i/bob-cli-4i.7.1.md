# Bead: bob-cli-4i.7.1 — Route the \`=x\` embedded-tree close through \`complete\_task\_tree\`

[Bead Pages](../README.md) / [bob-cli-4i.7](bob-cli-4i.7.md) / bob-cli-4i.7.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-4i.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-4i.land.md) · **Assignee:** `bob-cli-4i.7.1` · **Size:** medium
**Created:** 2026-10-05 18:10:31 EDT · **Closed:** 2026-10-05 18:28:26 EDT
**Plan:** [202610/bang\_task\_complete\_finish.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bang_task_complete_finish.md)

## Description

close_unify: in bob-cli, make `ClosePlanner::apply_embedded_tree` delegate its traversal to `task_complete::complete_task_tree` with `CloseLink` so one traversal remains. Keep every close test unchanged and `=x!N` output byte-identical. Make `Explicit` differ from `CloseLink` only at the root and in reporting recurring descendants. Stop reporting Canceled or Done descendants as left open. Remove unused `task_complete` re-exports.

## Notes

[2026-10-05T22:28:26Z · bob-cli-4i.7.1] close_unify done: apply_embedded_tree now drives one shared complete_embedded_trees traversal (CloseLink) and replays its visit log; descendants use CloseLink gate (Blocked/X never descended); Done/Canceled descendants neither closed nor reported; unused task_complete re-exports removed. Verified: cargo fmt clean, clippy has no new warnings (4 unused-import warnings gone, rest identical to base; only pre-existing bob-cli-28 deny remains), lib 1711 passed (only pre-existing bob-cli-4j kinds failure, reproduces on clean base), cli binary 991 passed incl. unchanged close suite and extended Blocked-embeds-open subtasks test.

## Dependencies

- **Blocks:** [bob-cli-4i.7.3](bob-cli-4i.7.3.md) ◐ · ⧖ 2026-10-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-4i.7.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-4i.7.1/README.md) | [bob-cli-4i.7.1](bob-cli-4i.7.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e0df2ea`](https://github.com/bobs-org/bob-cli/commit/e0df2ea621555149e48e4c26cbe390952b376ceb) | feat(close): route the =x embedded-tree close through complete\_task\_tree | [bob-cli-4i.7.1](bob-cli-4i.7.1.md) | 2026-10-05 18:29:14 EDT |
