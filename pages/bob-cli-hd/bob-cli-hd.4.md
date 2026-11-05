# Bead: bob-cli-hd.4 — Ledger Tools JS mirror, api.themes additions, and inherited type marks

[Bead Pages](../README.md) / [bob-cli-hd](README.md) / bob-cli-hd.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5q.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5q.linker.w0.md) · **Assignee:** `bob-cli-hd.4` · **Size:** medium
**Created:** 2026-11-05 10:26:34 EST · **Closed:** 2026-11-05 11:59:02 EST
**Plan:** [202611/pomodoro\_names\_follow\_task\_types.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/pomodoro_names_follow_task_types.md)

## Description

ledger-tools-mirror: copy the vectors, mirror `agreeEntry`, `settleClosed`, and the relocation MEET guard in JS, expose them and an async `agreeLedgerEntries` on api.themes, and let the type mark include inherited types.

## Notes

[2026-11-05T16:59:02Z · bob-cli-hd.4--2] Ledger Tools JS mirror verified: npm test 5485 pass/0 fail; npm run docs:check 447 passed 1 skipped; bob plugins sync deployed bob-ledger-tools main.js from workspace checkout (1 copied); sase bead epic-symbols clean.

## Dependencies

- **Depends on:** [bob-cli-hd.2](bob-cli-hd.2.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hd.7](bob-cli-hd.7.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hd.8](bob-cli-hd.8.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hd.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hd.4.md) | [bob-cli-hd.4](bob-cli-hd.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@b5bdd73`](https://github.com/bobs-org/bob-plugins/commit/b5bdd7354ab8acb7c05fc85ab1472d6aba42c84f) | feat(bob-ledger-tools): mirror ledger agree/settle planners, async api.themes applier, and inherited type marks | [bob-cli-hd.4](bob-cli-hd.4.md) | 2026-11-05 12:00:11 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hd.4--2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hd.4.md

<!-- sase:referenced-by:end -->
