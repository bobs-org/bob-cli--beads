# Bead: bob-cli-a2.10 — bob-ledger-tools LINKS and LINKED FROM chips

[Bead Pages](../README.md) / [bob-cli-a2](README.md) / bob-cli-a2.10

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.53.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.53.linker.w0.md) · **Assignee:** `bob-cli-a2.10` · **Size:** medium
**Created:** 2026-10-20 09:08:22 EDT · **Closed:** 2026-10-20 11:27:02 EDT
**Plan:** [202610/task\_relations.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_relations.md)

## Description

chips: render live chips for both relation rows in Live Preview and Reading view from the index, never the stored mirror. Add label pills, inverse phrases, ✓×N collapse, dashed stale and broken chips, and ＋ / × controls through nav api.relations. Reuse the bob-dep chip family with no new palette, and add LC tests.

## Notes

[2026-10-20T15:26:54Z · bob-cli-a2.10] PROPOSED FOLLOW-UP: 6 npm-test failures reproduce identically on clean master (4 unblocked-glyph incl. bob-cli-6v wall-clock cause, 1 decision-card keeps, 1 forward-promotion conversion)

[2026-10-20T15:27:02Z · bob-cli-a2.10] LC1-LC14 pass (17 new tests); focused 31 green; full suite shows only the 6 clean-master failures (noted follow-up); build/validate/inventory/docs-check pass; manifest 1.60.0 deployed via plugins sync; committed 03bb94b

## Dependencies

- **Blocks:** [bob-cli-a2.15](bob-cli-a2.15.md) ✓ · ⧖ 2026-10-20
- **Depends on:** [bob-cli-a2.8](bob-cli-a2.8.md) ✓ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-a2.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-a2.10/README.md) | [bob-cli-a2.10](bob-cli-a2.10.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@03bb94b`](https://github.com/bobs-org/bob-plugins/commit/03bb94b4b6a394a395588b6e92e8795514432af7) | feat(ledger-tools): render live LINKS and LINKED FROM chips | [bob-cli-a2.10](bob-cli-a2.10.md) | 2026-10-20 11:25:38 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a2.10][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-a2.10/README.md

<!-- sase:referenced-by:end -->
