# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.5 — List repeated completed Pomodoro names newest-first in start-name again rows

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.5` · **Size:** small
**Created:** 2026-10-25 11:34:35 EDT · **Closed:** 2026-10-25 12:04:03 EDT
**Plan:** [202610/backlog\_batch11\_ref\_repair\_taskcard\_popout\_gkeep\_again.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch11_ref_repair_taskcard_popout_gkeep_again.md)

## Description

start-name-again-order: resolve bob-cli-bn by making today_start_rows order again rows by latest occurrence, with an A, B, A regression in capture-complete JSON and the shell presenter, and shared vectors kept byte-identical with bob-plugins.

## Notes

[2026-10-25T16:03:53Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.5] start-name-again-order done: baseline today_start_rows replaced repeated key in first-seen slot then reversed, so A,B,A yielded B,A. Fix removes the old slot and pushes the newer entry (src/native/capture_complete/pomodoros.rs), so again rows are newest-first; Today ordering untouched. Added A,B,A regression pomodoro_start_name_orders_repeated_completed_names_newest_first asserting ALPHA precedes BETA in capture-complete JSON and in candidate_lines shell rows; verified it fails on the old code ([BETA, ALPHA]) and passes on the fix. Plugin mirror checked: 279-plugin-pomodoro-theme-mirrors.js mirrors theme ranking only and never orders again rows, no JS references pomodoro_start_name, vectors.json untouched, so no bob-plugins change or sync. just check passes. Leaving bob-cli-bn open for the lander; working tree has the two-file change uncommitted.

[2026-10-25T16:04:03Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.5] today_start_rows orders again rows newest-first (remove+push fix); A,B,A regression asserts ALPHA precedes BETA in capture-complete JSON and shell rows, fails on old code, passes on fix; just check green; no plugin/docs/fixture changes needed

## Dependencies

- **Depends on:** [bob-cli-an.6.6.6.5.6.5.5.6.6.6.3](bob-cli-an.6.6.6.5.6.5.5.6.6.6.3.md) ✓ · ⧖ 2026-10-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.5/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.5](bob-cli-an.6.6.6.5.6.5.5.6.6.6.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a8ef171`](https://github.com/bobs-org/bob-cli/commit/a8ef17181eaaa6b1ab31773fc55eaf79a8d0eff1) | fix(capture-complete): order repeated completed start names newest-first | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.5](bob-cli-an.6.6.6.5.6.5.5.6.6.6.5.md) | 2026-10-25 12:05:05 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.5][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.5/README.md

<!-- sase:referenced-by:end -->
