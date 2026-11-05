# Bead: bob-cli-hd.8 — Block ID Prompt writers and the task-status-cycler close

[Bead Pages](../README.md) / [bob-cli-hd](README.md) / bob-cli-hd.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5q.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5q.linker.w0.md) · **Assignee:** `bob-cli-hd.8` · **Size:** medium
**Created:** 2026-11-05 10:26:34 EST · **Closed:** 2026-11-05 12:43:01 EST
**Plan:** [202611/pomodoro\_names\_follow\_task\_types.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/pomodoro_names_follow_task_types.md)

## Description

prompt-and-cycler: block-id-prompt unlink, delete, and duplicate prune agree touched entries, and its new-entry picker retypes; the cycler close settles the closed name and keeps the continuation agreement-stable.

## Notes

[2026-11-05T17:38:58Z · bob-cli-hd.8--1] PROPOSED FOLLOW-UP: Stabilize strict performance budgets — Full npm test has variable timing-budget failures in block-id-prompt-task-wikilink-index-performance.cjs and ledger-tools-task-link-marks-live.cjs on both the phase tree and clean base, so these are unrelated to bob-cli-hd.8.

[2026-11-05T17:43:01Z · bob-cli-hd.8--1] Verified the Block ID Prompt and task-status-cycler implementation with the focused phase tests (including the fixed no-op cleanup expectations), generated build checks, passing npm run docs:check (447 passed, 1 skipped), and successful bob plugins sync --repo. Full npm test still hits variable performance-budget failures in unrelated suites; the same failures reproduce on the clean base, so they were recorded as a PROPOSED FOLLOW-UP. git diff --check passes and no epic symbols remain.

## Dependencies

- **Depends on:** [bob-cli-hd.4](bob-cli-hd.4.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hd.9](bob-cli-hd.9.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hd.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hd.8.md) | [bob-cli-hd.8](bob-cli-hd.8.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f36cc03`](https://github.com/bobs-org/bob-cli/commit/f36cc0396a7739941ef2ce85b61608c70f3d7333) | docs(memory): clarify merged Pomodoro type agreement | [bob-cli-hd.8](bob-cli-hd.8.md) | 2026-11-05 12:44:01 EST |
| bob-plugins | [`bob-plugins@6e30934`](https://github.com/bobs-org/bob-plugins/commit/6e30934999a89effab88776403e3cbba5af8b74f) | feat(pomodoro): align task types across prompt and close | [bob-cli-hd.8](bob-cli-hd.8.md) | 2026-11-05 12:44:22 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hd.8--1][1] | Need the phase scope, notes, and design file before completing validation | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hd.8.md

<!-- sase:referenced-by:end -->
