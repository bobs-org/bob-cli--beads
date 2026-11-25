# Bead: bob-cli-q4.10.1.4 — Task moves and splits settle every written note

[Bead Pages](../README.md) / [bob-cli-q4.10.1](bob-cli-q4.10.1.md) / bob-cli-q4.10.1.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q4.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.10.md) · **Assignee:** `bob-cli-q4.10.1.4` · **Size:** medium
**Created:** 2026-11-25 14:29:10 EST
**Plan:** [202611/navigation\_gesture\_settle.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/navigation_gesture_settle.md)

## Description

relocation: settle move source/destination and Task Split same-note, cross-note, created-note, and requirement-carry postimages before persistence. Return final anchors and exact settled receipts, preserve rollback and recovery, and keep moves following their destination while parking the walk. Cover routed moves that share writers.

## Dependencies

- **Depends on:** [bob-cli-q4.10.1.3](bob-cli-q4.10.1.3.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q4.10.1.5](bob-cli-q4.10.1.5.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q4.10.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.10.1.4.md) | [bob-cli-q4.10.1.4](bob-cli-q4.10.1.4.md) | 6 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@0e8c70b`](https://github.com/bobs-org/bob-plugins/commit/0e8c70b7fbbf65c33e4810ced2fdf17e4d9f1219) | feat(navigation): settle move and split postimages | [bob-cli-q4.10.1.4](bob-cli-q4.10.1.4.md) | 2026-11-25 17:14:50 EST |
| bob-plugins | [`bob-plugins@24dbb8a`](https://github.com/bobs-org/bob-plugins/commit/24dbb8a1e56b68701da356c5aac475e6132b0074) | test(navigation): respect live source path during split carry | [bob-cli-q4.10.1.4](bob-cli-q4.10.1.4.md) | 2026-11-25 17:24:16 EST |
| bob-plugins | [`bob-plugins@aecff7d`](https://github.com/bobs-org/bob-plugins/commit/aecff7d2463676b0232d901bd079bbcd2b92e175) | test(navigation): register open destination leaves in move fixtures | [bob-cli-q4.10.1.4](bob-cli-q4.10.1.4.md) | 2026-11-25 17:34:08 EST |
| bob-plugins | [`bob-plugins@f6167d4`](https://github.com/bobs-org/bob-plugins/commit/f6167d4c5bd47da44a33d11a7967c6848c0a9571) | test(bob-ledger-tools): await mention jump completion | [bob-cli-q4.10.1.4](bob-cli-q4.10.1.4.md) | 2026-11-25 18:09:25 EST |
| bob-cli | [`05dd83c`](https://github.com/bobs-org/bob-cli/commit/05dd83cf9f93c07825a30dfe508e530bc36f9d81) | docs: repair documentation gate consistency | [bob-cli-q4.10.1.4](bob-cli-q4.10.1.4.md) | 2026-11-25 18:31:13 EST |
| bob-plugins | [`bob-plugins@1c76c78`](https://github.com/bobs-org/bob-plugins/commit/1c76c782c8f48d8e1be7f66fe5dc74ca2a1bb0dc) | docs: trim plugin references below page budgets | [bob-cli-q4.10.1.4](bob-cli-q4.10.1.4.md) | 2026-11-25 18:31:56 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q4.10.1.4--1][1] | Need the phase scope, design, and recorded notes after monitored verification failed | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.10.1.4.md

<!-- sase:referenced-by:end -->
