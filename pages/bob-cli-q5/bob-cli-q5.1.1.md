# Bead: bob-cli-q5.1.1 — Snooze wake engine for bob-cli-q5.1

[Bead Pages](../README.md) / [bob-cli-q5.1](bob-cli-q5.1.md) / bob-cli-q5.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.1.md) · **Assignee:** `bob-cli-q5.1.1.land`
**Created:** 2026-11-25 10:36:15 EST · **Closed:** 2026-11-25 19:25:02 EST
**Plan:** [202611/snooze\_wake\_engine.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snooze_wake_engine.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/snooze_wake_engine.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snooze_wake_engine.md

<!-- sase:links:end -->

## Description

Complete bob-cli-q5.1 with a tested snooze CLI, safe never-running wake placement, shared row and time contracts, post-commit receipts and notices, first-position tick integration, and trailing-ledger-section preservation.

## Notes

[2026-11-26T00:06:52Z · bob-cli-q5.1.1.land] LAND TRIAGE of every PROPOSED FOLLOW-UP (checked on master 6a3e5df6): (a) wispr_summary kicker test (q5.1.1.1 #1, .2 #3, .4 #1, .5 #2) -> new task bob-cli-q9 (ci, small; pdftotext letter-spacing, test from closed bob-cli-pw). (b) x=build 'non-entry headline' panic (.5 #1) -> reproduced on HEAD, new task bob-cli-qa (bug, large), related to closed bob-cli-dq. (c) 17 tests/cli capture/ref_library/task_status_hooks failures (.2 #1, .4 #1, .5 #3) -> exact node set already a DISCOVERED ISSUE on active epic bob-cli-q4; fresh reproduction note added there. (d) docs budgets: bob-navigation-hotkeys 6039/6000 (.1 #2, .2 #4, .3 #1, .4 #2, .5 #4) -> +1 bob-cli-jz; plugin-apis 9322/8000 advisory -> +1 bob-cli-ob; capture-syntax 6086 and json-outputs 6032 -> caused by active epic bob-cli-q7 (4d930129, d883e564), DISCOVERED ISSUE note added there (json-outputs includes this epic's snooze row, trimmed 37->25 words by the lander). bob-ledger-tools overage (.2 #4, .5 #4) declined: no longer reported by docs-check at HEAD and bob-cli-il already tracks headroom. (e) declined as resolved at HEAD by 2d2f200d: REQUIREMENTS-casing lib tests three_component_marker and task_drawers_and_project_h2_drawers (.4 #1, .5 #2), capture_complete drawer bullet-menu tests (.2 #2), completion::capture_text (.5 #3); full cargo test --lib now fails only wispr_summary (8202/1). (f) landing discovery: clippy manual_contains break in tests/cli/capture/complete_block_id.rs:292 from d883e564 (bob-cli-q7.2) -> DISCOVERED ISSUE on bob-cli-q7.

[2026-11-26T00:25:02Z · bob-cli-q5.1.1.land] All five phases verified against plan:202611/snooze_wake_engine.md (row/clock/contracts, pure planners, guarded CLI, receipts/notify/tick, writer audit/vectors/docs).

Wake-refusal fix (this tale): plan_wake now returns Result<WakePlan, WakeRefusal> with no_pomodoros and multiple_open_timed; resolve_or_create_destination and untyped_destination return Result, InvalidPomodoroName maps to no_pomodoros, insert_subtree errors map to no_pomodoros; whole batch refuses before strike/prune (atomic, no partial batch); untyped path unchanged; wake-that-wakes-nothing never refuses. cli.rs maps WakeRefusal to CliError::refusal exit 2 with teaching copy; explicit, sweep, dry-run, initial and re-plan all refuse; nothing locked/written, no receipt/notify. plan.rs unit tests cover both refusals (no postimage) plus untyped-two-timed lands after first; wake vector runner accepts expected refusal. tests/cli/snooze.rs adds both CLI reproductions: exit 2, error kind, byte-identical daily, no last-wake.json, no notify.json (plus dry-run/explicit). docs/snooze.md Mutations plan_wake bullet and CLI paragraph state the refusal.

Lander integration edits (already committed at 03ca3f7e): snooze add settles notes via SettleContext (test add_settles_a_promoted_task_into_its_status_group); removed allow(unused_imports) re-export block in snooze/mod.rs, consumers use state::{classify_rows,live_targets}, when::parse_snooze_when, plan::{plan_add,plan_drop,plan_wake,plan_cleanup}, test-only move_subtree_to_entry_at is cfg(test); docs/snooze.md no longer calls CLI/receipts/tick follow-up phases and names parse_snooze_when; snooze row in reference/json-outputs.md trimmed.

Triage already recorded on epic: new tasks bob-cli-q9 (wispr kicker) and bob-cli-qa (x=build non-entry headline panic); +1 bob-cli-jz (nav hotkeys budget) and bob-cli-ob (plugin-apis); DISCOVERED ISSUE notes on bob-cli-q4 (17 settle-drift nodes) and bob-cli-q7 (clippy manual_contains + json budgets); declined bob-ledger-tools and resolved-at-HEAD items. No re-triage done here.

Checks: cargo fmt --all clean; just check stops at known clippy -D manual_contains in tests/cli/capture/complete_block_id.rs:292 from bob-cli-q7 (recorded, not fixed here); cargo test -p bob-obsidian --lib native::snooze 44 passed; cargo test -p bob-obsidian --test cli snooze 26 passed (incl 2 new refusal tests); tick 34 passed; wispr_summary single test fails as tracked by bob-cli-q9; ref_library::today fails as tracked settle-drift on bob-cli-q4; just docs-check lint ok, generated drift on docs/develop/decisions.md (pre-existing, untouched here), no snooze budget regression (snooze.md 2277 words, lint ok). No snooze or tick test fails.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.1.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.1.1.land.md) | [bob-cli-q5.1.1](bob-cli-q5.1.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`03ca3f7`](https://github.com/bobs-org/bob-cli/commit/03ca3f7e38f5708651c5351f305c586875466319) | feat(snooze): settle notes on add and retire unwired re-export allowances | [bob-cli-q5.1.1](bob-cli-q5.1.1.md) | 2026-11-25 19:09:08 EST |
| bob-cli | [`19e7fe5`](https://github.com/bobs-org/bob-cli/commit/19e7fe54e2a638c0856d3ded57e57b2947045fb9) | fix(snooze): refuse unplaceable wake destinations without writing | [bob-cli-q5.1.1](bob-cli-q5.1.1.md) | 2026-11-25 19:27:45 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.1.1.1][1] | Need parent epic scope and design decisions | 1 |
| read-by | [agent:bob-cli-q5.1.1.2][2] | Need parent epic DECISIONS and phase design | 1 |
| read-by | [agent:bob-cli-q5.1.1.4][3] | Need parent epic DECISIONS and land notes | 2 |
| read-by | [agent:bob-cli-q5.1.1.land][4] | Need the epic scope, children, and linked plan file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.1.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.1.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.1.1.4/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.1.1.land.md

<!-- sase:referenced-by:end -->
