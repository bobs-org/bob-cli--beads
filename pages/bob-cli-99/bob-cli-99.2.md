# Bead: bob-cli-99.2 — Board data path and pure lane models

[Bead Pages](../README.md) / [bob-cli-99](README.md) / bob-cli-99.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.8z](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.8z.md) · **Assignee:** `bob-cli-99.2` · **Size:** medium
**Created:** 2026-10-18 13:02:21 EDT · **Closed:** 2026-10-18 14:44:25 EDT
**Plan:** [202610/reading\_board.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/reading_board.md)

## Description

board-data: in bob-ledger-tools, share the stats spawn core, fetch and cache `bob ref list` JSON with stale-while-revalidate, and build the pure, tested lane, card, snoozed-group, ordering, and fence models.

## Notes

[2026-10-18T18:28:25Z · bob-cli-99.2] PROPOSED FOLLOW-UP: Record decisions:reading-board-is-bob-rendered after rollout — this epic selected memory_board_record=no; decide whether a new memory record is warranted after use.

[2026-10-18T18:28:31Z · bob-cli-99.2] PROPOSED FOLLOW-UP: Triage clean-base bob-plugins failures before the next green suite gate — npm test has 7 identical failures on our tree and clean base: four wall-clock unblocked-glyph cases (bob-cli-6v), Keep notice ordering (bob-cli-6w), the 16 ms ranker budget (bob-cli-3w), and forward/reverse BLOCKS conversion (bob-cli-7i).

[2026-10-18T18:44:10Z · bob-cli-99.2--1] PROPOSED FOLLOW-UP: Re-triage clean-base Highlights render tests failing in just all. The primary bob-cli checkout was clean at b88195e7: cargo test --lib failed pandoc_maps_every_contract_construct_to_tex, diagrams_swap_pdf_error_keeps_note_and_source, and diagrams_absent_results_match_unhooked_pdf; cargo test --test cli failed five highlights::diagrams Mermaid tests (2928 passed/3 failed in lib; 1768 passed/5 failed in cli). No primary source changed in this phase. Matching history: bob-cli-87.13 records the lifted-link failure; bob-cli-8y records Mermaid rendering and a prior green check.

[2026-10-18T18:44:25Z · bob-cli-99.2--1] Implemented and reviewed the shared bob spawn core, cached Reading Board data fetch, and pure lane/card/snoozed/fence models in bob-plugins; regenerated build is current, git diff --check passes, and both Reading Board suites pass (17/17). bob plugins sync reports the vault copy up to date. npm test reports only the seven previously recorded clean-base failures. just all fails in unchanged clean bob-cli at b88195e7 on 3 lib and 5 CLI Highlights render tests; recorded a PROPOSED FOLLOW-UP citing bob-cli-87.13 and bob-cli-8y. epic-symbols is empty.

## Dependencies

- **Depends on:** [bob-cli-99.1](bob-cli-99.1.md) ✓ · ⧖ 2026-10-18
- **Blocks:** [bob-cli-99.3](bob-cli-99.3.md) ✓ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-99.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-99.2.md) | [bob-cli-99.2](bob-cli-99.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@8a0be74`](https://github.com/bobs-org/bob-plugins/commit/8a0be74b5d590a5b3fcbb953b5b4e6fcd4086adb) | feat(reading-board): add board data and lane models | [bob-cli-99.2](bob-cli-99.2.md) | 2026-10-18 14:45:32 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-99.2--1][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-99.3][2] | Check phase 2 notes and what landed | 1 |
| read-by | [agent:bob-cli-99.land--2][3] | Reread child scope and all completion/triage notes before closing the Reading Board epic | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-99.2.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-99.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-99.land.md

<!-- sase:referenced-by:end -->
