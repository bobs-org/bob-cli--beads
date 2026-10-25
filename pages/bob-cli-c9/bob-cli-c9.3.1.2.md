# Bead: bob-cli-c9.3.1.2 — Resolve capture families and allocate complete reread bundles

[Bead Pages](../README.md) / [bob-cli-c9.3.1](bob-cli-c9.3.1.md) / bob-cli-c9.3.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-c9.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.3.md) · **Assignee:** `bob-cli-c9.3.1.2` · **Size:** medium
**Created:** 2026-10-25 15:22:58 EDT · **Closed:** 2026-10-25 16:58:17 EDT
**Plan:** [202610/ref\_create\_reread.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_create_reread.md)

## Description

family_planning: add shared capture-family classification, whole-bundle __vN allocation, and refusal metadata without enabling reread writes.

## Notes

[2026-10-25T20:58:17Z · bob-cli-c9.3.1.2] family_planning done, no reread writes enabled. New recapture.rs: URL-key exact-set resolution (1-URL-into-collection is partial, multi-reading exact set selects one family), stem resolution (free -N is ordinary), newest-first families with index-authoritative roots, __vN allocation from max+1 (>=2) through 999 with no _N fallback, -N/-o exit-2 errors with specified messages, newest-task defaults, reread: report line. duplicate.rs: reading vN segments, newest-first copies, unrendered next_stem. stamp.rs: occupancy extended (audio/.assets/sidecars/textbundle/ids) with recheck-ignoring-own-files; ordinary walk excludes audio to preserve the targeted audio refusal and force-overwrite-audio permission (2 pinned CLI audio tests green). Tests: 19 recapture + 9 duplicate unit tests incl. __v2/__v4->__v5, dangling middle, natural protocol__v2, real x__v2->x__v3, cap exhaustion, ambiguity. Gates: cargo fmt clean, clippy gate 0 errors, full cargo test 5744 passed 0 failed.

## Dependencies

- **Depends on:** [bob-cli-c9.3.1.1](bob-cli-c9.3.1.1.md) ✓ · ⧖ 2026-10-25
- **Blocks:** [bob-cli-c9.3.1.3](bob-cli-c9.3.1.3.md) ✓ · ⧖ 2026-10-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.3.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.3.1.2/README.md) | [bob-cli-c9.3.1.2](bob-cli-c9.3.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`347c36b`](https://github.com/bobs-org/bob-cli/commit/347c36b1c7add475a8a3a739dc1f024db7d7aebd) | feat(highlights): read-only family planning recapture with no reread writes | [bob-cli-c9.3.1.2](bob-cli-c9.3.1.2.md) | 2026-10-25 17:00:04 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-c9.3.1.2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.3.1.2/README.md

<!-- sase:referenced-by:end -->
