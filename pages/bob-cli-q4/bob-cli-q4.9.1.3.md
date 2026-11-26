# Bead: bob-cli-q4.9.1.3 — Settle promotion and committed open-line scaffolds

[Bead Pages](../README.md) / [bob-cli-q4.9.1](bob-cli-q4.9.1.md) / bob-cli-q4.9.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q4.9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.9.md) · **Assignee:** `bob-cli-q4.9.1.3` · **Size:** medium
**Created:** 2026-11-25 14:32:38 EST · **Closed:** 2026-11-25 16:28:49 EST
**Plan:** [202611/cycler\_gesture\_settle.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/cycler_gesture_settle.md)

## Description

structure-settle: compose promote and demote plans with settle in one transaction, and settle nonempty o/O scaffold commits while preserving empty-abandon and path guards.

## Notes

[2026-11-25T21:14:59Z · bob-cli-q4.9.1.3] PROPOSED FOLLOW-UP: docs-check lint budget overruns reproduce on this tree independently of structure-settle — plugin-apis.md 9279/8000, capture-syntax.md 6011/6000, bob-ledger-tools.md 6002/6000, bob-navigation-hotkeys.md 6068/6000; cycler/nav version inventory edits did not change those word counts

[2026-11-25T21:28:44Z · bob-cli-q4.9.1.3] PROPOSED FOLLOW-UP: just check bob-obsidian --lib (3) and --test cli (18) failures reproduce on the clean bob-cli tree this phase did not touch — already recorded on bob-cli-q5.1.1.2 citing bob-cli-q4 / bob-cli-q5.1.1.1 (capture grouping, wispr_summary, REQUIREMENTS drawer heading).

[2026-11-25T21:28:49Z · bob-cli-q4.9.1.3] structure-settle done. Cycler 1.63.0 mixin 144 composes promote/demote replace, replaceLines, and move with one staged taskSettle write (stay cursor plus jump; abandon on preimage/path/view/editor; fallback on missing or throwing provider). Counted ranges settle once. Nonempty o/O flush settles with joinHistory; empty prune stays byte-identical; reused-editor path drop; second flush inert. Regenerated stale nav 2.107.7 bundle and inventory so build:check and docs:inventory:check match HEAD source. Verified: 70/70 focused structure/open-line/promotion/demotion/counted tests; npm test 9637 pass 0 fail 4 skip plus 26 perf; build:check; docs:inventory:check; deployed task-status-cycler 1.63.0 without -F. epic-symbols empty. No memory edits. No ancestor closed. Pre-existing just check and docs-check overages recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-q4.9.1.2](bob-cli-q4.9.1.2.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q4.9.1.4](bob-cli-q4.9.1.4.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q4.9.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.9.1.3/README.md) | [bob-cli-q4.9.1.3](bob-cli-q4.9.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@1c2534c`](https://github.com/bobs-org/bob-plugins/commit/1c2534cc3ac5b3cfa6d86cf2d48ef213ee9b5805) | feat(task-status-cycler): settle promote/demote writes and nonempty o/O scaffolds | [bob-cli-q4.9.1.3](bob-cli-q4.9.1.3.md) | 2026-11-25 16:30:17 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q4.9.1.3][1] | Need the phase scope and design file | 4 |
| read-by | [agent:bob-cli-q4.9.1.land--7][2] | Need phase three verification scope for the q4.9.1 close note | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.9.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.9.1.land.md

<!-- sase:referenced-by:end -->
