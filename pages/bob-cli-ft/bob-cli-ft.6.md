# Bead: bob-cli-ft.6 — Block marks inside DEPENDS ON and BLOCKS chips

[Bead Pages](../README.md) / [bob-cli-ft](README.md) / bob-cli-ft.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.16w](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.16w.md) · **Assignee:** `bob-cli-ft.6` · **Size:** small
**Created:** 2026-11-02 06:28:11 EST · **Closed:** 2026-11-02 13:20:52 EST
**Plan:** [202611/blocked\_reason\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/blocked_reason_marks.md)

## Description

chips: a Blocked prerequisite or dependent chip draws its own miniature block mark and reason, exposing whether the critical path is waiting on work or on a date.

## Notes

[2026-11-02T18:20:52Z · bob-cli-ft.6] Implemented blocked-reason mini marks and reason text in DEPENDS ON and BLOCKS chips across Live Preview and reading view; rebuilt and synced bob-ledger-tools. Verified the focused dependency/blocks chip suites (34 passing), build:check, diff --check, and no remaining epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-ft.5](bob-cli-ft.5.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-ft.8](bob-cli-ft.8.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ft.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ft.6/README.md) | [bob-cli-ft.6](bob-cli-ft.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@93d3859`](https://github.com/bobs-org/bob-plugins/commit/93d3859988d3ebf6e03935bd8c541149f5f2f1a4) | feat(ledger-tools): show block reasons in dependency chips | [bob-cli-ft.6](bob-cli-ft.6.md) | 2026-11-02 13:21:23 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ft.6][1] | Check prior phase notes before continuing | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ft.6/README.md

<!-- sase:referenced-by:end -->
