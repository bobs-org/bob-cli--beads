# Bead: bob-cli-k3.5.1.1 — Render the records index and report its state

[Bead Pages](../README.md) / [bob-cli-k3.5.1](bob-cli-k3.5.1.md) / bob-cli-k3.5.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-k3.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.5.md) · **Assignee:** `bob-cli-k3.5.1.1` · **Size:** medium
**Created:** 2026-11-11 13:48:49 EST · **Closed:** 2026-11-11 14:37:10 EST
**Plan:** [202611/album\_records\_index.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_records_index.md)

## Description

index-rendering: share grouping and row ordering between the pure records renderer and album reports, plan the records region through host_catalog, and expose index state and stale findings with fixture coverage.

## Notes

[2026-11-11T19:36:57Z · bob-cli-k3.5.1.1] PROPOSED FOLLOW-UP: just docs-check fails on pre-existing reference word-budget overruns — capture-syntax.md, json-outputs.md, five mac-capture/plugin reference pages exceed the 6000-word cap on the clean base tree as well; this phase only added a few words to json-outputs.md.

[2026-11-11T19:37:10Z · bob-cli-k3.5.1.1] Rendered the bob-owned [!records] index as a pure function of declaration plus grouped folder members, planned through host_catalog BeforeFirstH2. list/check report index.state current/missing/stale/damaged without writing; missing/stale warn album_index_stale (bob albums sync), damaged errors album_index_damaged; check exits 0 on warning-only. cargo test --lib native::albums (51 passed) and --test cli albums (21 passed); cargo fmt --check and clippy lib/bin/tests with just check gates passed. No leftover --epic-symbol entries. just docs-check still fails on pre-existing reference word-budget overruns recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Blocks:** [bob-cli-k3.5.1.2](bob-cli-k3.5.1.2.md) ✓ · ⧖ 2026-11-11
- **Blocks:** [bob-cli-k3.5.1.3](bob-cli-k3.5.1.3.md) ✓ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-k3.5.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.5.1.1/README.md) | [bob-cli-k3.5.1.1](bob-cli-k3.5.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1f4c945`](https://github.com/bobs-org/bob-cli/commit/1f4c94571454ed9307094a677f69b31cddc30600) | feat(albums): render the records index and report its state | [bob-cli-k3.5.1.1](bob-cli-k3.5.1.1.md) | 2026-11-11 14:38:15 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-k3.5.1.1][1] | Need remaining description, notes, design, and DECISIONS | 2 |
| read-by | [agent:bob-cli-k3.5.1.3][2] | Check the earlier album phase's docs budget follow-up for existing ownership of this clean-base failure | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.5.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.5.1.3/README.md

<!-- sase:referenced-by:end -->
