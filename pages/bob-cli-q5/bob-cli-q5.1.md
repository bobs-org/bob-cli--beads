# Bead: bob-cli-q5.1 — bob snooze core, wake writer, and tick step

[Bead Pages](../README.md) / [bob-cli-q5](README.md) / bob-cli-q5.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fx](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fx.md) · **Assignee:** `bob-cli-q5.1` · **Size:** large
**Created:** 2026-11-25 10:22:52 EST · **Closed:** 2026-11-25 19:25:02 EST
**Plan:** [202611/snoozed\_tasks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snoozed_tasks.md)

## Description

wake-engine: the snooze module (row grammar, states, time grammar), the bob snooze list/add/drop/wake CLI with guarded writes, never-running wake placement, struck history rows, the first-position tick step, the wake receipt plus Darwin post plus desktop fallback, the trailing-section writer audit, shared vectors, and docs/snooze.md.

## Notes

[2026-11-25T15:33:48Z · bob-cli-q5.1] PLANNING: Inspected clean HEAD 814b6583 and the approved snoozed_tasks design; no prior phase notes or snooze implementation were present. Authored and validated a five-phase child epic (row-model, mutation-planners, guarded-cli, wake-delivery, writer-audit), preserving all outer decisions. The child land agent owns verification and closure of bob-cli-q5.1; no implementation changes or status changes made. No epic-symbol entries currently reference this phase. Existing routing runs first and subtree relocation appends, so explicit never-running/top-insertion variants are required.

[2026-11-26T00:26:10Z · bob-cli-q5.1.1.land] Child epic bob-cli-q5.1.1 (wake-engine) complete and verified; parent phase description items all hold:

- snooze module (row grammar, states, time grammar), CLI (list/add/drop/wake with guarded writes), never-running wake placement, struck history rows, first-position tick step, wake receipt plus Darwin post plus desktop fallback, trailing-section writer audit, shared vectors, docs/snooze.md.
- Passing checks: cargo fmt clean; cargo test -p bob-obsidian --lib native::snooze 44 passed; cargo test -p bob-obsidian --test cli snooze 26 passed (incl wake-refusal reproductions); tick 34 passed; tests/cli/snooze_writer_audit.rs passes (part of the 26). Known failures only: wispr_summary (bob-cli-q9), 17 settle-drift nodes (bob-cli-q4), clippy manual_contains from bob-cli-q7 (just check gate). No snooze or tick failure. Writer audit confirms ledger writers leave Snoozed bytes identical (LF/CRLF covered).
- Exposed APIs for bob-cli-q5.2 and bob-cli-q5.3: snooze::state::{classify_rows, live_targets}, snooze::when::parse_snooze_when, snooze::plan::{plan_add, plan_drop, plan_wake, plan_cleanup}, and routing::PlaceInput.never_running.
- Relative times round the offset up to five minutes (vector when-relative-45m: 13:02 + 45m -> 13:47), an interpretation of round up to the next 5 minutes that the outer phases should confirm before copying vectors.
- Remaining outer work: q5.2 planned-today readers, q5.3 capture z: token, plugin and Mac phases, glossary/guide, and live-vault acceptance. --note

[2026-11-26T00:26:20Z · bob-cli-q5.1.1.land] Phase verified via child epic bob-cli-q5.1.1 close: snooze module, guarded CLI, never-running placement with atomic wake refusal, struck history, first-position tick, receipt/Darwin/desktop, writer audit, shared vectors, docs/snooze.md. Checks: snooze lib 44 passed, snooze cli 26 passed, tick 34 passed; only known failures (wispr/bob-cli-q9, settle-drift/bob-cli-q4, clippy/bob-cli-q7). Exposed APIs and outer work recorded in prior note. Leaving epic bob-cli-q5 to its land agent.

## Dependencies

- **Blocks:** [bob-cli-q5.2](bob-cli-q5.2.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q5.3](bob-cli-q5.3.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.1.md) | [bob-cli-q5.1](bob-cli-q5.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.1.1.2][1] | Need the enclosing phase and final decisions | 1 |
| read-by | [agent:bob-cli-q5.1.1.4][2] | Need the enclosing phase and final decisions | 1 |
| read-by | [agent:bob-cli-q5.1.1.5][3] | Need enclosing phase decisions and scope | 1 |
| read-by | [agent:bob-cli-q5.1.1.land][4] | Need the parent phase scope, notes, and link for landing | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.1.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.1.1.4/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.1.1.5/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.1.1.land.md

<!-- sase:referenced-by:end -->
