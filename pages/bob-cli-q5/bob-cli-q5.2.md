# Bead: bob-cli-q5.2 — Snoozed rows in reconcile, walks, plan, and the agenda JSON

[Bead Pages](../README.md) / [bob-cli-q5](README.md) / bob-cli-q5.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fx](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fx.md) · **Assignee:** `bob-cli-q5.2` · **Size:** large
**Created:** 2026-11-25 10:22:52 EST · **Closed:** 2026-11-26 07:40:06 EST
**Plan:** [202611/snoozed\_tasks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snoozed_tasks.md)

## Description

planned-today: reconcile treats live rows as recovery-only reach and never touches them; freshness, ]s, and bob walks exclude snoozed tasks; bob plan gains the snoozed meter and forecast lint; capture-pomodoros --tasks gains additive snoozed rows and woke_at.

## Notes

[2026-11-26T00:32:42Z · bob-cli-q5.2] PLANNING: Checked clean baseline 03ca3f7e and the completed bob-cli-q5.1 handoff; core parser/classifier/writer APIs have landed, but none of this phase’s reader integrations are present and there were no prior phase implementation notes. Authored and validated a four-phase child epic: reader-recovery, review-exclusions, plan-forecast, agenda-provenance. Reconcile requires a separate direct snoozed recovery set because recent_activity_roots traverses dependencies; review must cover checklist and recurring overlays. Preserved all outer DECISIONS and agenda schema 1. The child epic land agent owns integrated verification and closure of bob-cli-q5.2 only. No product source, memory, or bead status changed. epic-symbols currently reports no entries for this phase.

[2026-11-26T12:41:39Z · bob-cli-q5.2.1.land] PARENT PHASE COMPLETION VERIFIED: the direct planned-today scope is fulfilled by the closed child epic: Snoozed rows recover directly without dependency promotion or Snoozed-section writes; freshness and walks exclude planned tasks; Today remains ledger-derived; hooks and bob plan forecasts agree for Snoozed-only notes; schema-1 agenda carries later-today rows and resolved wake provenance. Evidence: cargo test --test cli snoozed (31 passed), capture::pomodoros_agenda (25 passed), freshness (35 passed), and just docs-check (447 passed, one optional font skip). just check passed formatting and Clippy; its 43 library and 55 CLI failures match the existing 98-node clean-base record file:explicit:0bc82d5d4b7f7164deb53e4c, with representative drawer and Alpha grouping failures reproduced on untouched f32e774c. The child epic close automatically closed this phase as delegated work landed after its scope was verified; epic-symbols is empty. Containing epic bob-cli-q5 remains open for its lander.

## Dependencies

- **Depends on:** [bob-cli-q5.1](bob-cli-q5.1.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q5.4](bob-cli-q5.4.md) ◐ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q5.7](bob-cli-q5.7.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.2.md) | [bob-cli-q5.2](bob-cli-q5.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.1.1.land][1] | Check whether outer snooze phases consume wake-engine APIs before integration edits | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.1.1.land.md

<!-- sase:referenced-by:end -->
