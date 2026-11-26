# Bead: bob-cli-q5.4.1.4 — Link-now, unlink, and completion from snoozed contexts

[Bead Pages](../README.md) / [bob-cli-q5.4.1](bob-cli-q5.4.1.md) / bob-cli-q5.4.1.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.4.md) · **Assignee:** `bob-cli-q5.4.1.4` · **Size:** medium
**Created:** 2026-11-26 07:52:02 EST
**Plan:** [202611/snooze\_plugin\_plumbing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snooze_plugin_plumbing.md)

## Description

link-and-complete: integrate the shared model into block-id-prompt and task-status-cycler; distinguish snoozed presence from live-ledger presence, link immediately from the row or definition while moving notes, prune on unlink and Done, and test public gesture dispatch, stale snapshots, settle and undo.

## Dependencies

- **Depends on:** [bob-cli-q5.4.1.3](bob-cli-q5.4.1.3.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-q5.4.1.5](bob-cli-q5.4.1.5.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.4.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.4.1.4.md) | [bob-cli-q5.4.1.4](bob-cli-q5.4.1.4.md) | 5 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@1a65c42`](https://github.com/bobs-org/bob-plugins/commit/1a65c421395564b0d668cf9edfe8cab2a5aecc97) | feat(snoozed): link active rows to Pomodoros and prune on Done | [bob-cli-q5.4.1.4](bob-cli-q5.4.1.4.md) | 2026-11-26 10:16:35 EST |
| bob-plugins | [`bob-plugins@2744791`](https://github.com/bobs-org/bob-plugins/commit/274479191b06f18bb02aa1ad4494edba01e40577) | fix(snoozed-tasks): preserve note transfer during link-now | [bob-cli-q5.4.1.4](bob-cli-q5.4.1.4.md) | 2026-11-26 10:31:52 EST |
| bob-plugins | [`bob-plugins@4e0a8fd`](https://github.com/bobs-org/bob-plugins/commit/4e0a8fd0e96453a6c92ca8293dfa0c964d1f6111) | fix(plugins): preserve notes when linking snoozed tasks | [bob-cli-q5.4.1.4](bob-cli-q5.4.1.4.md) | 2026-11-26 10:42:06 EST |
| bob-plugins | [`bob-plugins@c534666`](https://github.com/bobs-org/bob-plugins/commit/c5346664d0584d8f93a5e36354a4992f41c8aa47) | fix(plugins): preserve link edits and repair full-test regressions | [bob-cli-q5.4.1.4](bob-cli-q5.4.1.4.md) | 2026-11-26 10:58:35 EST |
| bob-plugins | [`bob-plugins@db4bfd7`](https://github.com/bobs-org/bob-plugins/commit/db4bfd7ba2c58c22314ca15f58270fb99b5ceb4e) | fix(bob-ledger-tools): regenerate stale generated bundle | [bob-cli-q5.4.1.4](bob-cli-q5.4.1.4.md) | 2026-11-26 11:06:03 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.4.1.4--1][1] | Need the phase scope, notes, design file, and governing decisions | 1 |
| read-by | [agent:bob-cli-q5.4.1.4--2][1] | Review the assigned phase scope, verification gates, and close requirements | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.4.1.4.md

<!-- sase:referenced-by:end -->
