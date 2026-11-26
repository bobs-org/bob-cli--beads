# Bead: bob-cli-q5.4.1.3 — Navigation release, decay, and deferral cleanup

[Bead Pages](../README.md) / [bob-cli-q5.4.1](bob-cli-q5.4.1.md) / bob-cli-q5.4.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.4.md) · **Assignee:** `bob-cli-q5.4.1.3` · **Size:** medium
**Created:** 2026-11-26 07:52:02 EST · **Closed:** 2026-11-26 09:37:49 EST
**Plan:** [202611/snooze\_plugin\_plumbing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snooze_plugin_plumbing.md)

## Description

navigation-cleanup: compose active Snoozed-row removal into navigation cleanup and every release/cancel/roll/schedule/blocked-move/project-conversion caller; handle Alt+N on a Snoozed row and the Next-to-Ready decay writer, with transactional same-note and separate-note gesture tests.

## Notes

[2026-11-26T14:37:35Z · bob-cli-q5.4.1.3] PROPOSED FOLLOW-UP: obsidian-frontmatter-takeover-e2e --self-test fails identically on the clean base tree (modal root is not visible, focus is outside the modal) — environment UI issue unrelated to navigation-cleanup; no tracking bead found

[2026-11-26T14:37:49Z · bob-cli-q5.4.1.3] navigation-cleanup done: Snoozed-row removal composes into planDeferredPomodoroLinkCleanup (missing Pomodoros, closed entries, no ledger matches) with distinct removedSnoozedIdentities/LineRanges; all release/cancel/roll/schedule/blocked-move/conversion callers inherit it via changed; cursor repair (180/219/510/540/550/560/570) counts both passes; Alt+N on Snoozed rows runs the link release transaction (same-note fold + separate-note verified); 548 Next-to-Ready folds/prunes, WIP-to-Next preserves snooze; 14 new tests pass; lane/decay/cancel/project/relation/review suites green; validate + docs:check green; full unit 9902/9907 with the single frontmatter e2e self-test failing identically on clean base (recorded as follow-up); bob plugins sync deployed

## Dependencies

- **Depends on:** [bob-cli-q5.4.1.2](bob-cli-q5.4.1.2.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-q5.4.1.4](bob-cli-q5.4.1.4.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.4.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.4.1.3/README.md) | [bob-cli-q5.4.1.3](bob-cli-q5.4.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@1770259`](https://github.com/bobs-org/bob-plugins/commit/1770259cf0b3088d640d44cf00d16027af23a7a2) | feat(navigation): compose Snoozed-row removal into deferred cleanup, Alt+N, and decay \| Snoozed-row explicit removal composes into planDeferredPomodoroLinkCleanup with distinct reporting; offset callers count both passes; Alt+N on a Snoozed row releases through the link transaction; Next-to-Ready decay folds the cleanup while WIP-to-Next preserves the snooze; 14 regression tests. \| SASE\_BEAD=\[bob-cli-q5.4.1.3\] | [bob-cli-q5.4.1.3](bob-cli-q5.4.1.3.md) | 2026-11-26 09:39:07 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.4.1.3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.4.1.3/README.md

<!-- sase:referenced-by:end -->
