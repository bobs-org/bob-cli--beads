# Bead: bob-cli-e8.8 — Nav courtesy writes, stage rows, refusals, and counts

[Bead Pages](../README.md) / [bob-cli-e8](README.md) / bob-cli-e8.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2v.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2v.linker.w0.md) · **Assignee:** `bob-cli-e8.8` · **Size:** medium
**Created:** 2026-10-29 17:20:22 EDT · **Closed:** 2026-10-29 19:41:23 EDT
**Plan:** [202610/inline\_task\_mentions.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/inline_task_mentions.md)

## Description

plugin-nav: write mention mirrors when the cursor leaves an edited line, show mentions in the Linked-from stage and Task Card count, refuse removal and reserved labels, and downgrade unlinked pairs.

## Notes

[2026-10-29T23:41:00Z · bob-cli-e8.8] PROPOSED FOLLOW-UP: 5 task-card theme tests fail identically on the clean base tree (test-navigation-task-card-theme-edit.cjs: theme notices, no-op batches, save notices, stage-row subtitle; plus theme-menu-grey in test-navigation-task-card-view.cjs), apparently from e8.5s theme-pill change; unrelated to e8.8, left red

[2026-10-29T23:41:23Z · bob-cli-e8.8] nav phase done: reserved 💬 label in grammar/parsers/writers with reserved-message refusals; linked_from_mentions loader (default false); mirrorMentionHandEdit courtesy write (pair diff + touched-source M7/mint/uncertainty, same-note transaction + cross-note follow-ups) hooked into fireDependencyHandEditMirror; unlink downgrade in applyRelationEdit/removeAll with unlink notice; Linked-from stage from linkedFrom() v2 with mention rows (pill/excerpt/open/refuse/footer hints) + Task Card N/R/M counts + notice-text updates. Tests: new test-navigation-relation-mentions.cjs (31 pass, registered in package.json); full npm test 4303/4308 with only the 5 pre-existing theme failures (recorded as follow-up); build:check, docs:check, and plugins sync (nav + block-id-prompt from this checkout; ledger-tools left at e8.6 d096507) all green

## Dependencies

- **Depends on:** [bob-cli-e8.5](bob-cli-e8.5.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-e8.9](bob-cli-e8.9.md) ◐ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-e8.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e8.8/README.md) | [bob-cli-e8.8](bob-cli-e8.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@7366cfd`](https://github.com/bobs-org/bob-plugins/commit/7366cfdd33029d5a6017a70845ed9e096bf0de3b) | feat(navigation): inline task-mention courtesy writes, stage rows, and unlink downgrade | [bob-cli-e8.8](bob-cli-e8.8.md) | 2026-10-29 19:43:43 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-e8.8][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e8.8/README.md

<!-- sase:referenced-by:end -->
