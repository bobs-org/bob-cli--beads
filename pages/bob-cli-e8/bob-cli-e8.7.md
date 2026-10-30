# Bead: bob-cli-e8.7 — Mention context card and embed-echo suppression

[Bead Pages](../README.md) / [bob-cli-e8](README.md) / bob-cli-e8.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2v.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2v.linker.w0.md) · **Assignee:** `bob-cli-e8.7` · **Size:** medium
**Created:** 2026-10-29 17:20:22 EDT · **Closed:** 2026-10-29 19:55:59 EDT
**Plan:** [202610/inline\_task\_mentions.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/inline_task_mentions.md)

## Description

plugin-card: add the accessible why-is-this-here card on each mention pill and hide embedded-in entries inside their own host's transclusion.

## Notes

[2026-10-29T23:53:34Z · bob-cli-e8.7] PROPOSED FOLLOW-UP: Restore the full bob-plugins npm test suite to green — npm test fails identically on clean base d096507 and this phase tree: four missing taskCardTheme* helpers in scripts/test-navigation-task-card-theme-edit.cjs plus the is-muted assertion in scripts/test-navigation-task-card-view.cjs; searched for an existing bead tracking these failures and found none (related closed bob-cli-dm.7.1.1 does not track them).

[2026-10-29T23:55:59Z · bob-cli-e8.7] Implemented accessible mention context cards and filtered host-note embed echoes. Verified plugin build, 26/26 targeted relation-chip tests, synced main.js/styles.css match the linked checkout, git diff --check clean, and no epic symbols. Full npm test has five failures reproduced identically on clean base d096507; recorded them as a PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-e8.6](bob-cli-e8.6.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-e8.9](bob-cli-e8.9.md) ✓ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-e8.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e8.7/README.md) | [bob-cli-e8.7](bob-cli-e8.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@90dbc6a`](https://github.com/bobs-org/bob-plugins/commit/90dbc6a1c302e2fa6e89668a53ad274c519a6892) | feat(mentions): add accessible context cards and embed echo suppression | [bob-cli-e8.7](bob-cli-e8.7.md) | 2026-10-29 19:56:57 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-e8.7][1] | Inspect phase notes to see whether earlier work left a remainder | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e8.7/README.md

<!-- sase:referenced-by:end -->
