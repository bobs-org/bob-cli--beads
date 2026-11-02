# Bead: bob-cli-f6.6 — bob-plugins: render #untracked and keep Obsidian keymaps in lockstep

[Bead Pages](../README.md) / [bob-cli-f6](README.md) / bob-cli-f6.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bv](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bv.md) · **Assignee:** `bob-cli-f6.6` · **Size:** medium
**Created:** 2026-11-01 11:24:14 EST · **Closed:** 2026-11-01 17:40:30 EST
**Plan:** [202611/untracked\_calendar\_events.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/untracked_calendar_events.md)

## Description

plugins-untracked: paint #untracked on Event rows, keep \p and home chips untracked-aware, and mirror MEET starts per the decision.

## Notes

[2026-11-01T22:40:22Z · bob-cli-f6.6] PROPOSED FOLLOW-UP: five bob-plugins tests fail identically on the clean base tree (2026-11-01) — test-command-mode-sheet-sequence-dom "production sheet render and clicks use real DOM APIs", test-ledger-tools-freshness-namespace "the reload event fires only when the due key set changes", test-ledger-tools-gcal-events "create listener runs once for today's note after layout readiness", test-ledger-tools-note-ready "the startup storm is linear", test-ledger-tools-relation-index "relationIndex registers after layout-ready..."; likely date- or startup-timing-sensitive, unrelated to #untracked.

[2026-11-01T22:40:30Z · bob-cli-f6.6] bob-plugins (bob-ledger-tools 1.82.0): Event painter paints #untracked (timer-off mark, dashed time pill, Live Preview + Reading view); N\p/N\P keep untracked rows untracked (N\o/N\O and Ctrl+Enter regression-tested); untracked home chips dashed with 'untracked · not counted' tooltip (pomodoro_homes vectors already byte-identical to bob-cli); se<X>+Tab on a MEET follows the event run + [t::] rule and Notices mirror pomodoro_event_run_later / pomodoro_runs_past_event for se/\p/\o/\O, driven by byte-copied meet_event_run vectors (15 mirrored, 3 capture-only). event_task_close vectors have no untracked case upstream, so none added. Verified: npm test = 4840/4845 pass (5 failures reproduce identically on the clean base tree; noted as PROPOSED FOLLOW-UP), build:check, validate, docs:check green; deployed via bob plugins sync --repo -p bob-ledger-tools. No memory notes edited; no epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-f6.2](bob-cli-f6.2.md) ✓ · ⧖ 2026-11-01
- **Depends on:** [bob-cli-f6.3](bob-cli-f6.3.md) ✓ · ⧖ 2026-11-01
- **Depends on:** [bob-cli-f6.4](bob-cli-f6.4.md) ✓ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-f6.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-f6.6/README.md) | [bob-cli-f6.6](bob-cli-f6.6.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-f6.6][1] | Need the phase scope and design file | 1 |
| read-by | [agent:research.2z.cld][2] | Check in-flight untracked phases before recommending a representation change | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-f6.6/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.2z.cld/README.md

<!-- sase:referenced-by:end -->
