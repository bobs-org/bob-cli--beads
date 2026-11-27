# Bead: bob-cli-q5.6.1.2 — Resolve snooze targets and commit guarded note edits

[Bead Pages](../README.md) / [bob-cli-q5.6.1](bob-cli-q5.6.1.md) / bob-cli-q5.6.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.6.md) · **Assignee:** `bob-cli-q5.6.1.2` · **Size:** medium
**Created:** 2026-11-27 01:34:15 EST · **Closed:** 2026-11-27 02:47:02 EST
**Plan:** [202611/snooze\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snooze_card.md)

## Description

runtime: resolve supported cursor contexts, apply same-note and cross-note plans safely, provide card facts, and delegate explicit Wake now to bob.

## Notes

[2026-11-27T07:46:49Z · bob-cli-q5.6.1.2] PROPOSED FOLLOW-UP: 6 bob-plugins e2e self-tests fail with ENOSPC because /tmp is full (32G tmpfs shared with other agents); verified identical failure on the clean base tree (git stash -u). Affected: test-obsidian-block-marks-e2e, test-obsidian-command-chips-e2e, test-obsidian-command-chips-keymap-e2e, test-obsidian-copy-chips-e2e, plus 2 DOM/CSS self-tests in the full run. Re-run when /tmp has space.

[2026-11-27T07:46:53Z · bob-cli-q5.6.1.2] PROPOSED FOLLOW-UP: bob-plugins and bob-cli docs:check lint fails on docs/reference/vault-format.md word budget (6030/6000); verified identical failure on the clean base tree. File untouched by snooze phases; needs a docs-budget decision or trim.

[2026-11-27T07:47:02Z · bob-cli-q5.6.1.2] Runtime controller landed: nav 683 resolve/740-class pure target resolution (definition/live/woken/history/snoozed-row, multi_task/prose/ambiguous/fenced/needs_naming refusals), never-running wake destination projection, card facts with unavailable providers, wake report policy; 686 guarded commit mixin (one editor transaction per open note, vault.process preimage for closed, cross-note rollback only while postimage intact, midnight revalidation, duplicate-submit guard, review advance, no spawn on add/drop, bob-only wake with view.save flush and 8s Notice only for unannounced nonempty wokes) exposed via api.snoozeRuntime v1; ledger snoozeFacts v1 adapter (zone/date/clock/events/activeRow/planCounts). Verified: 30 new tests pass, 104 focused snooze tests pass, full unit 10201 pass (6 unrelated ENOSPC e2e failures, clean-tree identical, filed as follow-up), build:check + validate pass, git diff --check clean, bob plugins sync deployed both bundles. Full bob-cli just check exceeded the turn window with all observed tests passing and zero Rust changes; docs:check lint failure is pre-existing (follow-up filed).

## Dependencies

- **Depends on:** [bob-cli-q5.6.1.1](bob-cli-q5.6.1.1.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-q5.6.1.3](bob-cli-q5.6.1.3.md) ✓ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.6.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.6.1.2/README.md) | [bob-cli-q5.6.1.2](bob-cli-q5.6.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@6a61e16`](https://github.com/bobs-org/bob-plugins/commit/6a61e163c850a53a415ab75db374075814f7c327) | feat(snooze): add runtime target resolution and guarded commit controller | [bob-cli-q5.6.1.2](bob-cli-q5.6.1.2.md) | 2026-11-27 02:47:51 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.6.1.2][1] | Need the phase scope and notes | 2 |
| read-by | [agent:bob-cli-q5.6.1.3][2] | Need runtime controller interface for card phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.6.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.6.1.3/README.md

<!-- sase:referenced-by:end -->
