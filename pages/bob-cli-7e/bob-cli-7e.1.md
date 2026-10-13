# Bead: bob-cli-7e.1 — The BLOCKS-line contract, managed-line registry, and vectors

[Bead Pages](../README.md) / [bob-cli-7e](README.md) / bob-cli-7e.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4d.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4d.linker.w0.md) · **Assignee:** `bob-cli-7e.1` · **Size:** medium
**Created:** 2026-10-13 11:09:49 EDT · **Closed:** 2026-10-13 11:24:23 EDT
**Plan:** [202610/prerequisite\_blocks\_lines.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prerequisite_blocks_lines.md)

## Description

contract: write docs/task-dependencies.md §14 (grammar, membership, minting, order, position, authority, writers, gestures, chips, kill switch, outputs), grow §2.4 into the managed-child-line registry, add the BK/BR/BW/BC/MC vectors, and align projects.md, capture.md, and getting-started.md.

## Notes

[2026-10-13T15:24:23Z · bob-cli-7e.1] Wrote docs/task-dependencies.md §14 (vocabulary, grammar, membership, minting, order, position, reconciliation, writers, gestures, chips, kill switch, outputs, rollout) with BK1–BK21, BR1–BR29, BW1–BW19, BC1–BC15; grew §2.4 into the managed-child-line registry and added MC1–MC9 in §11.8; aligned projects.md (Sub-projects after Depends-On and BLOCKS, MC8 move rule), capture.md (`&` staging plus dependency-drop BLOCKS updates, blocks_line_updates, minted_dependent_block_id), and getting-started.md (dependencies.blocks_lines). Glyph is brick throughout. No leftover --epic-symbol entries. New §14 heading anchors resolve. Memory left to rollout (glossary authorized but owned by that phase).

[2026-10-13T15:37:38Z · bob-cli-7e.1--1] PROPOSED FOLLOW-UP: just check fails the two percent-listen CLI tests already tracked by bob-cli-6m (capture::r#ref::failed_percent_listen_worker_keeps_listen_retry_guidance at tests/cli/capture/ref.rs:991; percent_listen_reference_runs_existing_worker_and_installs_audio at ref.rs:942). ToolRun 446f8b18764d7970cf3f27bb5f58225f / monitor 4jaqsvr11mbz: 1465 passed, 2 failed; listen.log never written. Docs-only dirty tree; identical to clean-base reports on bob-cli-6m.

## Dependencies

- **Blocks:** [bob-cli-7e.2](bob-cli-7e.2.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-7e.3](bob-cli-7e.3.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-7e.4](bob-cli-7e.4.md) ✓ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-7e.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-7e.1.md) | [bob-cli-7e.1](bob-cli-7e.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4f72e5c`](https://github.com/bobs-org/bob-cli/commit/4f72e5c513317708f098b35e2dfd4beab82b5748) | docs(tasks): contract BLOCKS lines, managed-child registry, and vectors | [bob-cli-7e.1](bob-cli-7e.1.md) | 2026-10-13 11:39:06 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7e.1--1][1] | Need the phase scope, design file, notes, and remaining work | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-7e.1.md

<!-- sase:referenced-by:end -->
