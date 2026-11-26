# Bead: bob-cli-q5.1.1 — Snooze wake engine for bob-cli-q5.1

[Bead Pages](../README.md) / [bob-cli-q5.1](bob-cli-q5.1.md) / bob-cli-q5.1.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.1.md) · **Assignee:** `bob-cli-q5.1.1.land`
**Created:** 2026-11-25 10:36:15 EST
**Plan:** [202611/snooze\_wake\_engine.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snooze_wake_engine.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/snooze_wake_engine.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snooze_wake_engine.md

<!-- sase:links:end -->

## Description

Complete bob-cli-q5.1 with a tested snooze CLI, safe never-running wake placement, shared row and time contracts, post-commit receipts and notices, first-position tick integration, and trailing-ledger-section preservation.

## Notes

[2026-11-26T00:06:52Z · bob-cli-q5.1.1.land] LAND TRIAGE of every PROPOSED FOLLOW-UP (checked on master 6a3e5df6): (a) wispr_summary kicker test (q5.1.1.1 #1, .2 #3, .4 #1, .5 #2) -> new task bob-cli-q9 (ci, small; pdftotext letter-spacing, test from closed bob-cli-pw). (b) x=build 'non-entry headline' panic (.5 #1) -> reproduced on HEAD, new task bob-cli-qa (bug, large), related to closed bob-cli-dq. (c) 17 tests/cli capture/ref_library/task_status_hooks failures (.2 #1, .4 #1, .5 #3) -> exact node set already a DISCOVERED ISSUE on active epic bob-cli-q4; fresh reproduction note added there. (d) docs budgets: bob-navigation-hotkeys 6039/6000 (.1 #2, .2 #4, .3 #1, .4 #2, .5 #4) -> +1 bob-cli-jz; plugin-apis 9322/8000 advisory -> +1 bob-cli-ob; capture-syntax 6086 and json-outputs 6032 -> caused by active epic bob-cli-q7 (4d930129, d883e564), DISCOVERED ISSUE note added there (json-outputs includes this epic's snooze row, trimmed 37->25 words by the lander). bob-ledger-tools overage (.2 #4, .5 #4) declined: no longer reported by docs-check at HEAD and bob-cli-il already tracks headroom. (e) declined as resolved at HEAD by 2d2f200d: REQUIREMENTS-casing lib tests three_component_marker and task_drawers_and_project_h2_drawers (.4 #1, .5 #2), capture_complete drawer bullet-menu tests (.2 #2), completion::capture_text (.5 #3); full cargo test --lib now fails only wispr_summary (8202/1). (f) landing discovery: clippy manual_contains break in tests/cli/capture/complete_block_id.rs:292 from d883e564 (bob-cli-q7.2) -> DISCOVERED ISSUE on bob-cli-q7.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.1.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.1.1.land/README.md) | [bob-cli-q5.1.1](bob-cli-q5.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`03ca3f7`](https://github.com/bobs-org/bob-cli/commit/03ca3f7e38f5708651c5351f305c586875466319) | feat(snooze): settle notes on add and retire unwired re-export allowances | [bob-cli-q5.1.1](bob-cli-q5.1.1.md) | 2026-11-25 19:09:08 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.1.1.1][1] | Need parent epic scope and design decisions | 1 |
| read-by | [agent:bob-cli-q5.1.1.2][2] | Need parent epic DECISIONS and phase design | 1 |
| read-by | [agent:bob-cli-q5.1.1.4][3] | Need parent epic DECISIONS and land notes | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.1.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.1.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.1.1.4/README.md

<!-- sase:referenced-by:end -->
