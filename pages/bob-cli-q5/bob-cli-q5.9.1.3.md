# Bead: bob-cli-q5.9.1.3 — Make the Obsidian planner replace struck history on re-snooze

[Bead Pages](../README.md) / [bob-cli-q5.9.1](bob-cli-q5.9.1.md) / bob-cli-q5.9.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1hl](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1hl.md) · **Assignee:** `bob-cli-q5.9.1.3` · **Size:** small
**Created:** 2026-11-27 20:55:08 EST · **Closed:** 2026-11-27 21:21:37 EST
**Plan:** [202611/finish\_snoozed\_tasks\_unattended.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_snoozed_tasks_unattended.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:0967234d84f65c3a6aa0baa1 | attached via sase artifact create --bead |
| related | file:explicit:6950613a72aac0ae70eaee93 | attached via sase artifact create --bead |
| related | file:explicit:911c05c5ff222ecee2d83ad0 | attached via sase artifact create --bead |
| related | file:explicit:a41139bbc36016e4710d695a | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

plugin-resnooze: align the bob-navigation-hotkeys snooze planner with bob's canonical re-snooze rule, flip the two tests that pinned the split, verify in real Obsidian, and deploy.

## Notes

[2026-11-28T02:21:18Z · bob-cli-q5.9.1.3] plugin-resnooze landed in bob-plugins (HEAD 145b4a3d plus uncommitted planner/docs/e2e). snoozeMutationUpsertRow now mirrors bob-cli upsert_active_row: no matching active row removes the last matching struck history row and its subtree without carrying those children; matching active rows are retimed and history stays. Flipped planner test re-snoozing a woken task replaces its struck wake-history receipt; added retiming-keeps-history case. e2e check resnooze-replaces-struck-history-and-closed-ledger-history-stays: struck Snoozed row replaced, closed ledger [[jobs#^history]] block untouched. Docs: task-card.md and bob-navigation-hotkeys.md. q5 discovered issues 4-6 (JS planner keeping struck history on re-snooze) fixed here.

Verified: npm run build; node --test test-navigation-snooze-mutation-planner + test-snooze-model-vectors (21/21 plus extra planner case) + remaining snooze unit tests; npm run docs:check passed; npm test 10454 pass / 1 fail / 4 skip then perf 28/28. The one fail is ranker cpu clock charges cpu work, not descheduling (test-navigation-dependencies-stage-entry-and-view.cjs) — 50 ms parked sleep charged 24.09 ms CPU (budget 16 ms); reran twice green. Known flake bob-cli-3w. Real Obsidian xvfb-run -a scripts/obsidian-snooze-card-e2e.cjs PASS 60/60 with workspace debug bob befff97c. Report file:explicit:911c05c5ff222ecee2d83ad0; screenshots file:explicit:a41139bbc36016e4710d695a file:explicit:6950613a72aac0ae70eaee93 file:explicit:0967234d84f65c3a6aa0baa1. e2e scratch root moved to /tmp/bob-sn-e2e so Chromium SingletonSocket fits. bob plugins sync --repo this checkout --no-pull -p bob-navigation-hotkeys copied main.js.

[2026-11-28T02:21:23Z · bob-cli-q5.9.1.3] PROPOSED FOLLOW-UP: ranker cpu clock flake under parallel npm test — test-navigation-dependencies-stage-entry-and-view.cjs "ranker cpu clock charges cpu work, not descheduling" failed once (50 ms parked sleep charged 24.09 ms CPU, budget 16 ms) then passed twice in isolation; already tracked by bob-cli-3w.

[2026-11-28T02:21:37Z · bob-cli-q5.9.1.3] Verified: snoozeMutationUpsertRow mirrors upsert_active_row (replace last matching struck history on re-snooze; retime keeps history). Planner tests, snooze vectors 21/21, docs-check, real Obsidian xvfb e2e PASS 60/60 (file:explicit:911c05c5ff222ecee2d83ad0). npm test one unrelated ranker-cpu flake (bob-cli-3w). Deployed bob-navigation-hotkeys via bob plugins sync. q5 notes 4-6 fixed. No leftover --epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-q5.9.1.9](bob-cli-q5.9.1.9.md) ◐ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.9.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.9.1.3/README.md) | [bob-cli-q5.9.1.3](bob-cli-q5.9.1.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.9.1.3][1] | Need the phase scope, notes, design file, and epic DECISIONS | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.9.1.3/README.md

<!-- sase:referenced-by:end -->
