# Bead: bob-cli-eq.1 — Shared task wikilink rules and parity vectors

[Bead Pages](../README.md) / [bob-cli-eq](README.md) / bob-cli-eq.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.b5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.b5.md) · **Assignee:** `bob-cli-eq.1` · **Size:** medium
**Created:** 2026-10-30 16:10:20 EDT · **Closed:** 2026-10-30 16:47:28 EDT
**Plan:** [202610/obsidian\_task\_wikilinks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/obsidian_task_wikilinks.md)

## Description

model: pin bob's wikilink_task pool, order, link-target, and guard rules as shared vectors asserted in bob-cli, and mirror them in a pure block-id-prompt model.

## Notes

[2026-10-30T20:46:59Z · bob-cli-eq.1] PROPOSED FOLLOW-UP: Write decisions:obsidian-task-wikilinks-mirror-bob explaining why the Obsidian (( picker mirrors bob rules in JS instead of spawning bob (plan decision decision_record=no skipped it)

[2026-10-30T20:47:08Z · bob-cli-eq.1] PROPOSED FOLLOW-UP: Fix pre-existing npm failures test-ledger-tools-relation-index (relation scan after layout-ready) and test-ledger-tools-note-ready (startup storm is linear); both reproduce identically on the clean tree without eq.1 changes

[2026-10-30T20:47:13Z · bob-cli-eq.1] PROPOSED FOLLOW-UP: Run bob plugins sync for block-id-prompt at integration time; skipped now because the live vault holds sibling phase eq.2 trigger fragment 022-task-wikilink-token.js and -F would clobber it

[2026-10-30T20:47:28Z · bob-cli-eq.1] Model phase done: 12-vector fixture (tests/fixtures/task_wikilinks/vectors.json) asserted by Rust vectors test (17/17 lib tests incl. vectors_match_candidates_and_link_targets); mirrored verbatim to bob-plugins with pure 031/032 model fragments and 12/12 JS tests incl. sha256 pin; just check sections all green (fmt/clippy/lib/integration/doc, no failures); npm validate green; full npm test 4425 pass with 2 pre-existing failures reproduced on clean tree (noted as follow-ups); plugins sync deliberately skipped to protect sibling eq.2 vault deployment (noted)

## Dependencies

- **Blocks:** [bob-cli-eq.3](bob-cli-eq.3.md) ✓ · ⧖ 2026-10-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-eq.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-eq.1/README.md) | [bob-cli-eq.1](bob-cli-eq.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ebd74b7`](https://github.com/bobs-org/bob-cli/commit/ebd74b7b7a21b3888623651a54997fbe9cea2550) | feat(capture): add task-wikilink ranker vectors and candidates tests | [bob-cli-eq.1](bob-cli-eq.1.md) | 2026-10-30 16:51:08 EDT |
| bob-plugins | [`bob-plugins@9dd0374`](https://github.com/bobs-org/bob-plugins/commit/9dd0374e2d19dd5397a9887d2e7b07561d146bdc) | feat(block-id-prompt): mirror task-wikilink rank model with vectors and tests | [bob-cli-eq.1](bob-cli-eq.1.md) | 2026-10-30 17:04:25 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-eq.1][1] | Need full phase detail including notes | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-eq.1/README.md

<!-- sase:referenced-by:end -->
