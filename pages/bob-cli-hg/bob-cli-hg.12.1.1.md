# Bead: bob-cli-hg.12.1.1 — Compose note model and new/reply commands

[Bead Pages](../README.md) / [bob-cli-hg.12.1](bob-cli-hg.12.1.md) / bob-cli-hg.12.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-hg.12](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.12.md) · **Assignee:** `bob-cli-hg.12.1.1` · **Size:** medium
**Created:** 2026-11-06 07:12:29 EST · **Closed:** 2026-11-06 08:16:04 EST
**Plan:** [202611/gmail\_compose.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_compose.md)

## Description

compose-notes: implement the source-region model, safe note creation, reply/all insertion, CLI exclusions, and preservation tests in section 4.1.

## Notes

[2026-11-06T13:15:20Z · bob-cli-hg.12.1.1] PROPOSED FOLLOW-UP: Refresh the stale README contract-table snapshot hash; just docs-check fails at tools/docs/tests/test_contracts.py::test_readme_table_matches_original_contract_index_snapshot although the exact same table hash is present on clean HEAD (96a429d5f5b7eb02484e4806dac0ca688e41858e3187dfbdb26ad994a6107e4a). This is already recorded at bob-cli-hg.6.1.4 note #1 and bob-cli-hl.3.1.5 note #1.

[2026-11-06T13:16:04Z · bob-cli-hg.12.1.1] Implemented local compose source parsing, safe new/reply note writes, exact-path commits, public CLI/help/docs with Bob Mail catalog exclusions, and preservation/symlink/offline tests. Verified: cargo check --tests; compose source unit tests 7/7; Gmail shell tests 36/36; catalog exclusion test; cargo fmt and git diff --check; just docs-gen. just docs-check passed all gates through tutorial/media but its docs unit suite has one clean-HEAD README contract-table snapshot failure (446 passed, 1 failed, 1 skipped), recorded as a proposed follow-up and already tracked in bob-cli-hg.6.1.4 note #1 / bob-cli-hl.3.1.5 note #1. epic-symbols: no entries.

## Dependencies

- **Blocks:** [bob-cli-hg.12.1.2](bob-cli-hg.12.1.2.md) ✓ · ⧖ 2026-11-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.12.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.12.1.1/README.md) | [bob-cli-hg.12.1.1](bob-cli-hg.12.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2a37f8c`](https://github.com/bobs-org/bob-cli/commit/2a37f8ce073d8e166590daec83412ad6e49671d8) | feat(gmail): add offline compose and reply notes | [bob-cli-hg.12.1.1](bob-cli-hg.12.1.1.md) | 2026-11-06 09:24:02 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hg.12.1.1][1] | Confirm whether this phase has prior work notes | 2 |
| read-by | [agent:bob-cli-hg.12.1.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.12.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.12.1.land/README.md

<!-- sase:referenced-by:end -->
