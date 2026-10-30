# Bead: bob-cli-eq.5 — Name-then-link for ID-less tasks

[Bead Pages](../README.md) / [bob-cli-eq](README.md) / bob-cli-eq.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.b5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.b5.md) · **Assignee:** `bob-cli-eq.5` · **Size:** small
**Created:** 2026-10-30 16:10:20 EDT · **Closed:** 2026-10-30 18:36:23 EDT
**Plan:** [202610/obsidian\_task\_wikilinks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/obsidian_task_wikilinks.md)

## Description

naming: the Block ID prompt's wikilink mode, its back-to-picker lifecycle, closed-task support, and stale-line relocation.

## Notes

[2026-10-30T22:32:53Z · bob-cli-eq.5] PROPOSED FOLLOW-UP: Decide whether to add decisions:obsidian-task-wikilinks-mirror-bob explaining the JS mirror rationale — the epic selected decision_record=no, so no memory note was changed.

[2026-10-30T22:36:23Z · bob-cli-eq.5] Implemented ID-less (( naming, picker-state restoration, closed-task support, and unique exact-line relocation. Focused naming/picker/submit/prefill tests: 59 passed; build:check and docs:check passed; epic-symbols reported no leftovers. Plugin sync was attempted and refused by the deployment safety guard because the vault contains an uncommitted build from another checkout; no force overwrite was made.

## Dependencies

- **Depends on:** [bob-cli-eq.4](bob-cli-eq.4.md) ✓ · ⧖ 2026-10-30
- **Blocks:** [bob-cli-eq.6](bob-cli-eq.6.md) ✓ · ⧖ 2026-10-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-eq.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-eq.5/README.md) | [bob-cli-eq.5](bob-cli-eq.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@458907b`](https://github.com/bobs-org/bob-plugins/commit/458907b3aa6f8030503fa4d70dbd2693da513c0b) | feat(block-id-prompt): name-then-link for ID-less tasks | [bob-cli-eq.5](bob-cli-eq.5.md) | 2026-10-30 18:43:07 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-eq.5][1] | Need phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-eq.5/README.md

<!-- sase:referenced-by:end -->
