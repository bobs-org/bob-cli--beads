# Bead: bob-cli-go.12 — Bob Mac Capture transfer spans, bands, and verbs

[Bead Pages](../README.md) / [bob-cli-go](README.md) / bob-cli-go.12

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.36.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.36.linker.w0.md) · **Assignee:** `bob-cli-go.12` · **Size:** medium
**Created:** 2026-11-03 16:11:31 EST · **Closed:** 2026-11-04 11:39:40 EST
**Plan:** [202611/task\_move\_merge\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_move_merge_split.md)

## Description

mac: style the transfer spans, render bob's moves[] and merges[] as Moves and Merges preview bands, show the Move or Merge footer verb, and write notification copy, while staying a thin client.

## Notes

[2026-11-04T16:18:11Z · bob-cli-go.12--1] PROPOSED FOLLOW-UP: Fix the generated task-merge glossary strand front matter so docs-check generated-drift validation passes; the same exit-2 error reproduces on a pristine base copy after lint passes. Tracking bead: bob-cli-go.13 (closeout: docs and accepted memory).

[2026-11-04T16:39:40Z · bob-cli-go.12--2] Transfer UI implementation verified on fresh scratch copies: Mac bundle and typecheck-tests pass; Athena portable-check passes (2,095 tests, 1 skipped). Docs lint passes; generated task-merge glossary front-matter drift reproduces on pristine base and is recorded as follow-up citing bob-cli-go.13. Epic symbols clear.

## Dependencies

- **Depends on:** [bob-cli-go.11](bob-cli-go.11.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-go.13](bob-cli-go.13.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-go.12](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-go.12.md) | [bob-cli-go.12](bob-cli-go.12.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@81eb669`](https://github.com/bobs-org/bob-mac-capture/commit/81eb669406cc9a72d3eca8d936543617bbd450f7) | feat(capture): preview task transfers in Mac Capture | [bob-cli-go.12](bob-cli-go.12.md) | 2026-11-04 11:41:04 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-go.12--2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-go.12.md

<!-- sase:referenced-by:end -->
