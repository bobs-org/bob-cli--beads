# Bead: bob-cli-eq.2 — Note grammar for the (( trigger

[Bead Pages](../README.md) / [bob-cli-eq](README.md) / bob-cli-eq.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.b5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.b5.md) · **Assignee:** `bob-cli-eq.2` · **Size:** small
**Created:** 2026-10-30 16:10:20 EDT · **Closed:** 2026-10-30 16:26:19 EDT
**Plan:** [202610/obsidian\_task\_wikilinks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/obsidian_task_wikilinks.md)

## Description

trigger: pure (( token detection for Markdown notes, its note-only exclusions, and the written-second-paren auto-open rule, pinned by vectors.

## Notes

[2026-10-30T20:25:57Z · bob-cli-eq.2] PROPOSED FOLLOW-UP: bob-plugins npm test shows 2 failures in scripts/test-ledger-tools-relation-index.cjs ("the startup storm is linear", "relationIndex registers after layout-ready and never reads non-markdown during startup replay"); both reproduce identically on the clean base tree (verified via git stash) and are already tracked by task bead bob-cli-eh (type ci), corroborated with +1 there. Not caused by this phase.

[2026-10-30T20:26:07Z · bob-cli-eq.2] PROPOSED FOLLOW-UP: add the bob-cli decisions strand decisions:obsidian-task-wikilinks-mirror-bob in the review phase (this phase skipped it because the epic DECISIONS set decision_record = no, which forbids editing that memory here).

[2026-10-30T20:26:19Z · bob-cli-eq.2] Trigger phase done: pure (( token detection (022-task-wikilink-token.js), trigger_vectors.json fixture, and test-block-id-prompt-task-wikilink-token.cjs (9 tests green). Gates: npm run build, focused suite, all 406 block-id-prompt tests, npm run validate green; full npm test has only the 2 pre-existing relation-index failures tracked by bob-cli-eh (repro on clean base, +1 there); bob plugins sync deployed, vault converged. No behavior wired yet, per plan.

## Dependencies

- **Blocks:** [bob-cli-eq.4](bob-cli-eq.4.md) ✓ · ⧖ 2026-10-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-eq.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-eq.2/README.md) | [bob-cli-eq.2](bob-cli-eq.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@27acd61`](https://github.com/bobs-org/bob-plugins/commit/27acd61630e576e9964ab9639fe09b5c96762fc3) | feat(block-id-prompt): pure (( trigger grammar with vectors and tests | [bob-cli-eq.2](bob-cli-eq.2.md) | 2026-10-30 16:27:23 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-eq.2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-eq.2/README.md

<!-- sase:referenced-by:end -->
