# Bead: bob-cli-q7.2 — bob-cli: Go rows for @route^ completion, mint-collision copy, and /route^id search

[Bead Pages](../README.md) / [bob-cli-q7](README.md) / bob-cli-q7.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1g6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1g6.md) · **Assignee:** `bob-cli-q7.2` · **Size:** medium
**Created:** 2026-11-25 15:25:24 EST · **Closed:** 2026-11-25 18:15:36 EST
**Plan:** [202611/caret\_address\_goto\_capture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/caret_address_goto_capture.md)

## Description

cli-browse: add the additive block_id.goto rows to task_block_id completion for bare @route^ and partial IDs, teach the new form in the mint-collision error, index route^id in the / search fields, and document all three.

## Notes

[2026-11-25T23:15:19Z · bob-cli-q7.2] PROPOSED FOLLOW-UP: just check stays red on clean master — 3 lib failures (three_component_marker drawer case, task_merge drawers, wispr summary words), 18 CLI failures (inbox_route x2, note_pull x3, project_note x3, project_note_offer x6, task_theme_writes, completion drawers_after_id_hash, ref today theme, task_status_hooks sync), plus a wall-clock flake in september_shaped_vault_finishes_fast under parallel load. All reproduce identically with this phase stashed.

[2026-11-25T23:15:25Z · bob-cli-q7.2] PROPOSED FOLLOW-UP: just docs-check lint fails on clean master — 4 word-budget errors (develop plugin-apis, capture-syntax at 6058/6000, json-outputs, bob-ledger-tools, bob-navigation-hotkeys). This phase adds ~30 words to already-over capture-syntax.md; the failure reproduces with this phase stashed.

[2026-11-25T23:15:36Z · bob-cli-q7.2] cli-browse done: block_id.goto Go rows on whole-draft @route^/@route^partial (doc order, dupes omitted, archive rows flagged, unfiltered, missing note eligible with no rows), mint-collision error teaches @route^id, / picker matches route^id. Verified: 8 new CLI completion tests + caret_browse unit + caret ranker unit green; affected suites 98 lib + 182 CLI green; fmt clean, clippy gates 0 errors. Full-suite and docs-check failures reproduce identically on clean master (recorded as PROPOSED FOLLOW-UPs); no epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-q7.1](bob-cli-q7.1.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q7.5](bob-cli-q7.5.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q7.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q7.2/README.md) | [bob-cli-q7.2](bob-cli-q7.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d883e56`](https://github.com/bobs-org/bob-cli/commit/d883e564ecac1aecc9c3b6d4a1c72517cae87379) | feat(capture): scoped browse block\_id.goto with archive rows, mint-collision hint, route^block-id search | [bob-cli-q7.2](bob-cli-q7.2.md) | 2026-11-25 18:16:48 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.7.1.land--7][1] | Verify independent clean-baseline docs budget overage corroboration | 1 |
| read-by | [agent:bob-cli-q5.1.1.land][2] | Check whether the complete_block_id manual_contains lint break is tracked by its landing | 1 |
| read-by | [agent:bob-cli-q7.2][3] | Need phase scope | 2 |
| read-by | [agent:bob-cli-q7.5--1][4] | Check pre-existing just check clippy entry cited by q7.5 follow-up | 1 |
| read-by | [agent:bob-cli-q8.land][5] | Lander q8: confirm q8.1's claim that q7.2 notes track the two pre-existing lib failures | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ph.7.1.land.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.1.1.land.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q7.2/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q7.5.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q8.land/README.md

<!-- sase:referenced-by:end -->
