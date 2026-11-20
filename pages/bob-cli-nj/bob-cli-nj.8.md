# Bead: bob-cli-nj.8 — Decision record, glossary term, and cross-repo docs sweep

[Bead Pages](../README.md) / [bob-cli-nj](README.md) / bob-cli-nj.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.f3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.f3.md) · **Assignee:** `bob-cli-nj.8` · **Size:** small
**Created:** 2026-11-19 12:14:03 EST · **Closed:** 2026-11-19 20:13:29 EST
**Plan:** [202611/log\_reason\_recall.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/log_reason_recall.md)

## Description

recall-memory: write the Log Recall decision record and glossary term through /sase_memory_write, citing the landed commits. Verify that docs/log-recall.md, the plugin reference, and the Mac docs agree with the shipped behavior.

## Notes

[2026-11-20T01:13:29Z · bob-cli-nj.8] Verified the Log Recall contract and Mac Capture docs against landed behavior; added Rotten single/decay/batch keep and successor Cancel recall coverage to the plugin reference. npm run docs:check passed, bob plugins sync completed, and epic-symbols reported no leftovers. Epic reviewer decisions prohibit decision/glossary memory edits.

## Dependencies

- **Depends on:** [bob-cli-nj.3](bob-cli-nj.3.md) ✓ · ⧖ 2026-11-19
- **Depends on:** [bob-cli-nj.4](bob-cli-nj.4.md) ✓ · ⧖ 2026-11-19
- **Depends on:** [bob-cli-nj.7](bob-cli-nj.7.md) ✓ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-nj.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nj.8/README.md) | [bob-cli-nj.8](bob-cli-nj.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@3d1f553`](https://github.com/bobs-org/bob-plugins/commit/3d1f553fc07a49faa0acfc07d9b4068380f41ba4) | docs(log-recall): cover plugin prompt surfaces | [bob-cli-nj.8](bob-cli-nj.8.md) | 2026-11-19 20:14:59 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nj.8][1] | Confirm the assigned phase closed after verification | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nj.8/README.md

<!-- sase:referenced-by:end -->
