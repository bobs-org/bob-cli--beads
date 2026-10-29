# Bead: bob-cli-dm.7.1.2 — Edit task themes through the Task Card

[Bead Pages](../README.md) / [bob-cli-dm.7.1](bob-cli-dm.7.1.md) / bob-cli-dm.7.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-dm.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dm.7.md) · **Assignee:** `bob-cli-dm.7.1.2` · **Size:** medium
**Created:** 2026-10-28 22:50:54 EDT · **Closed:** 2026-10-28 23:31:40 EDT
**Plan:** [202610/task\_card\_successor\_themes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_card_successor_themes.md)

## Description

card-theme-edit: add the t stage and Ctrl+D use-default with API-backed field setters and guarded local, counted, and linked task edits that preserve status, links, and freshness.

## Notes

[2026-10-29T03:31:40Z · bob-cli-dm.7.1.2] Implemented card-theme-edit in bob-plugins: t/Enter opens a Theme stage (Use default first with inherited reason, then Today/Recent/typed new, deduped, query/selection preserved; unknown inherited selectable), Ctrl+D on the Theme row clears to default via clear-theme intent (field clearing, never hide), t added to repeated-action suppression. Direct-edit planner validates typed names, uses catalog spelling, enforces single non-exempt component, Use-default/inherited clears, same-key no-op, repair handling. Guarded local/counted/linked writes use only setTaskTheme/clearTaskTheme with identity+line preimage and inherited revalidation, one undo for local/counted, per-note guarded writes with honest partial failures for linked; closed tasks skipped, no status/link/ID/freshness/schedule/WorkLog/walk effects, review walk suppressed. Updated model/view expectations, added scripts/test-navigation-task-card-theme-edit.cjs (8 tests), registered in package.json, updated docs/task-card.md and docs/bob-navigation-hotkeys.md. Verified: npm run build + build:check clean, 126 focused task-card tests pass, full npm test 4156 pass, npm run validate clean, npm run docs:check passed. Deploy: bob plugins sync for bob-navigation-hotkeys refused by provenance guard (deployed from uncommitted build in workspace bob-cli_14, c59819c); did not force with -F, left for land agent. No manual desktop verification (Obsidian UI not reachable); header/pill/t/Enter/Ctrl+D/cancellation covered by tests.

## Dependencies

- **Depends on:** [bob-cli-dm.7.1.1](bob-cli-dm.7.1.1.md) ✓ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-dm.7.1.3](bob-cli-dm.7.1.3.md) ✓ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-dm.7.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.7.1.2/README.md) | [bob-cli-dm.7.1.2](bob-cli-dm.7.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@1c9e0e1`](https://github.com/bobs-org/bob-plugins/commit/1c9e0e13750457248f1ce282c77b34db348e0283) | feat(navigation): edit task themes through the Task Card | [bob-cli-dm.7.1.2](bob-cli-dm.7.1.2.md) | 2026-10-28 23:32:38 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-dm.7.1.2][1] | full read | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.7.1.2/README.md

<!-- sase:referenced-by:end -->
