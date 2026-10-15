# Bead: bob-cli-7x.7 — RefsCore rename contract, fetcher, stores, and card state

[Bead Pages](../README.md) / [bob-cli-7x](README.md) / bob-cli-7x.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.1k.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.1k.linker.w0.md) · **Assignee:** `bob-cli-7x.7` · **Size:** medium
**Created:** 2026-10-15 15:25:59 EDT · **Closed:** 2026-10-15 17:33:44 EDT
**Plan:** [202610/bob\_ref\_rename.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_ref_rename.md)

## Description

mac-rename-core: in bob-mac-capture RefsCore, decode the ref rename report, add RefsFetching.rename on a non-cancelling refs-rename lane, map older-bob and error envelopes, add RefsOpenLogStore.rename(from:to:), pure rename-card state, key map, and presentation strings; fake-bob branch and portable tests.

## Notes

[2026-10-15T21:33:44Z · bob-cli-7x.7--5] Implemented reference rename decoding, non-cancelling fetch lane, error mapping, open-log path updates, and rename card state/presentation with fixtures and portable tests; removed temporary fixture instrumentation. Bob Mac Capture just portable-check passed on athena, and epic-symbol check reported none.

## Dependencies

- **Depends on:** [bob-cli-7x.3](bob-cli-7x.3.md) ✓ · ⧖ 2026-10-15
- **Blocks:** [bob-cli-7x.8](bob-cli-7x.8.md) ✓ · ⧖ 2026-10-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7x.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7x.7.md) | [bob-cli-7x.7](bob-cli-7x.7.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8a3c561`](https://github.com/bobs-org/bob-cli/commit/8a3c5613393c5ec253c3f6ae3d5f0bec51ab3948) | docs(refs): record rename identity decision | [bob-cli-7x.7](bob-cli-7x.7.md) | 2026-10-15 17:45:59 EDT |
| bob-mac-capture | [`bob-mac-capture@da2d0ef`](https://github.com/bobs-org/bob-mac-capture/commit/da2d0efdaa4b6c2c357b8ca8a6030163ca406b9a) | feat(refs): add Bob Refs rename support | [bob-cli-7x.7](bob-cli-7x.7.md) | 2026-10-15 17:55:55 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7x.7--5][1] | Resume assigned phase closure and confirm its scope and recorded notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7x.7.md

<!-- sase:referenced-by:end -->
