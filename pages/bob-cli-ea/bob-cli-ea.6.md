# Bead: bob-cli-ea.6 — bob gcal sync writes Events rows and MEET links

[Bead Pages](../README.md) / [bob-cli-ea](README.md) / bob-cli-ea.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2w.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2w.linker.w0.md) · **Assignee:** `bob-cli-ea.6` · **Size:** medium
**Created:** 2026-10-29 19:40:04 EDT · **Closed:** 2026-10-30 01:57:19 EDT
**Plan:** [202610/bob\_gcal\_daily\_events.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_gcal_daily_events.md)

## Description

gcal-sync: render Event Task and context rows, keep the per-host journal, plan inserts, adoption, tombstones, and the appended MEET placeholder with links written once, write through a locked preimage-checked transaction with a no-op guarantee, and ship sync, list's VAULT column, docs, and the daily-note decision record.

## Notes

[2026-10-30T05:57:19Z · bob-cli-ea.6] bob gcal sync ships: Events rows + MEET links via locked preimage-checked transaction with no-op guarantee; verified by 17 sync acceptance tests, 35 gcal unit tests, full lib suite 4018 green, docs-gen/docs-check green. Also fixed 2 pre-existing red contract tests (catalog count, day completion kind). 3 clippy gate errors remain, all pre-existing on the base tree in untouched files.

## Dependencies

- **Depends on:** [bob-cli-ea.1](bob-cli-ea.1.md) ✓ · ⧖ 2026-10-29
- **Depends on:** [bob-cli-ea.2](bob-cli-ea.2.md) ✓ · ⧖ 2026-10-29
- **Depends on:** [bob-cli-ea.5](bob-cli-ea.5.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-ea.7](bob-cli-ea.7.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-ea.8](bob-cli-ea.8.md) ✓ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ea.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ea.6/README.md) | [bob-cli-ea.6](bob-cli-ea.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`98f9a23`](https://github.com/bobs-org/bob-cli/commit/98f9a23ad26f92df23ca9c6fc6b789353a3bd3a4) | feat(gcal): add bob gcal sync | [bob-cli-ea.6](bob-cli-ea.6.md) | 2026-10-30 02:24:20 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ea.6][1] | Need full phase description, notes, and remaining work | 2 |
| read-by | [agent:bob-cli-ea.land][2] | Need the child scope and notes | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ea.6/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ea.land/README.md

<!-- sase:referenced-by:end -->
