# Bead: bob-cli-on.4 — The bob task tidy command

[Bead Pages](../README.md) / [bob-cli-on](README.md) / bob-cli-on.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ex](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ex.md) · **Assignee:** `bob-cli-on.4` · **Size:** medium
**Created:** 2026-11-21 11:13:26 EST · **Closed:** 2026-11-21 14:11:28 EST
**Plan:** [202611/task\_requirements.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_requirements.md)

## Description

task-tidy: add `bob task tidy`, a previewed, one-commit repair of open task blocks into canonical order that moves whole subtrees and files loose notes of requirement-owning tasks into NOTES.

## Notes

[2026-11-21T19:10:42Z · bob-cli-on.4] PROPOSED FOLLOW-UP: docs-check still fails identically on the clean base — lint word-budget caps on docs/reference/plugins/bob-navigation-hotkeys.md and docs/reference/vault-format.md, plus strict-build anchor task-dependencies.md#1224-js--jump-successor-contract-and-vectors from capture.md; already recorded on bob-cli-on.3 and bob-cli-oe.2. task-tidy pages pass lint and the new #34-tidying-task-blocks anchor resolves in the built site.

[2026-11-21T19:11:16Z · bob-cli-on.4] PROPOSED FOLLOW-UP: flaky test — tests/cli albums_update::completion_offers_update_stems_and_input_files failed once (stems: []) inside the full parallel just check run and passed 3/3 alone on the unchanged tree; same flake already noted on bob-cli-on.3.

[2026-11-21T19:11:28Z · bob-cli-on.4] Shipped bob task tidy [ROUTE...] (-a/--apply, -b/--bob-dir, -f/--format human|json — human matches every other bob command; -h). New src/native/task_tidy/: tidy_note runs task_block_layout::plan_tidy over every open task top to bottom, rescanning after each repair so nested subtasks moved by a parent are repaired in the same pass; closed tasks and done/, _generated/, _templates/ are never touched; ROUTE = capture route or vault-relative path, unknown_route/route_out_of_scope exit 2. Dry run prints per-task colored before/after excerpts grouped by note plus "{t} tasks in {n} notes · {m} moves · {s} notes filed under NOTES"; JSON schema_version 1. -a uses host_catalog::run_locked (lock, pre-sync, replan, preimage-guarded writes, verify that nothing replans, one "bob task tidy (N tasks in M notes)" commit, post-sync). Planning refuses any note whose repair would drop or invent a line or would not settle. Wired into runner, completion (ROUTE → Route kind), catalog exclusion, help fixtures; docs: task-requirements.md §3.4, json-outputs row, regenerated CLI pages. Verified: 12 unit tests + 5 tests/cli/task_tidy.rs CLI tests (dry run, apply + idempotent rerun, routes, no-op); just check green except a known flake that passes alone; docs lint/build/links show only pre-existing failures; read-only dry run on ~/bob: 5760 notes, 576 open tasks, 2.7s debug, 1 planned move. Sibling bob-cli-on.5 also edits TASK_MEMBERS, TASK_AFTER_HELP, and tests/fixtures/help — expect a trivial merge.

## Dependencies

- **Depends on:** [bob-cli-on.3](bob-cli-on.3.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-on.5](bob-cli-on.5.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.4/README.md) | [bob-cli-on.4](bob-cli-on.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f888213`](https://github.com/bobs-org/bob-cli/commit/f888213a22650dd6e33b38e9f77e7a65ca8e24e6) | feat(task): add bob task tidy to repair open task blocks | [bob-cli-on.4](bob-cli-on.4.md) | 2026-11-21 14:12:31 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-o6.6.1.5][1] | Check whether the running plugin phase owns the offer_close fixture sync | 1 |
| read-by | [agent:bob-cli-on.4][2] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-o6.6.1.5/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.4/README.md

<!-- sase:referenced-by:end -->
