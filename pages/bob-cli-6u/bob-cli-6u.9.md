# Bead: bob-cli-6u.9 — Capture never links a Blocked task

[Bead Pages](../README.md) / [bob-cli-6u](README.md) / bob-cli-6u.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.70](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.70.md) · **Assignee:** `bob-cli-6u.9` · **Size:** medium
**Created:** 2026-10-12 10:26:02 EDT · **Closed:** 2026-10-12 16:50:48 EDT
**Plan:** [202610/prj\_line\_project\_blocking.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_project_blocking.md)

## Description

cli-capture-links: link-toggle consumption at every plan_task_link caller, the gesture rule (date-blocked ^prj refused), and unlinked tagged [?] results for new tasks in blocked projects, @route:id s:N, and blocked + projects.

## Notes

[2026-10-12T20:50:31Z · bob-cli-6u.9] PROPOSED FOLLOW-UP: wall-clock-rotted fixtures fail on base too — task_status_hooks_reconciles_future_schedules_and_combined_blocking_reasons (blocked.rs:173, expects 7 got 11) and projects_sync_then_task_status_hooks_blocks_and_recovers_propagated_tasks (schedule.rs:131, July 2026 dates now past); reproduced identically on clean master 2026-10-12, also noted on bob-cli-6u.13

[2026-10-12T20:50:36Z · bob-cli-6u.9] PROPOSED FOLLOW-UP: capture r#ref percent-listen worker tests fail without the listen helper binary (env, tracked by bob-cli-6m); reproduced on clean master 2026-10-12

[2026-10-12T20:50:48Z · bob-cli-6u.9] cli-capture-links done: staged-graph link guard at all 4 plan_task_link callers (toggle, ensure-next, @r:id, close-link) with PDG1/PDG3 consume+promote+not_linked report, PDG6 date-only ^prj refusal, PDG2 pull-forward preserved; new : tasks unlinked when Blocked (s:N, open &, blocked project → [?]+tag); + projects tag+unlink : tasks when P>today; additive link_guard JSON + human trailer; docs/capture.md rows. Verified: cargo fmt clean, clippy 0 errors, lib 2431 pass, cli 1388 pass; only 4 failures reproduce identically on clean base (2 r#ref listen env per bob-cli-6m, 2 wall-clock-rotted July fixtures) recorded as PROPOSED FOLLOW-UP. No --epic-symbol leftovers.

## Dependencies

- **Blocks:** [bob-cli-6u.16](bob-cli-6u.16.md) ✓ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.17](bob-cli-6u.17.md) ✓ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.4](bob-cli-6u.4.md) ✓ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.8](bob-cli-6u.8.md) ✓ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.9/README.md) | [bob-cli-6u.9](bob-cli-6u.9.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`36f997b`](https://github.com/bobs-org/bob-cli/commit/36f997b1aad6d0757b83de36aff75f584718237d) | feat(capture): never link a Blocked task | [bob-cli-6u.9](bob-cli-6u.9.md) | 2026-10-12 16:52:38 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:72][1] | Assess 6u phase state and deps for conflict analysis with 6t | 1 |
| read-by | [agent:bob-cli-6u.8][2] | Need epic and children status | 1 |
| read-by | [agent:bob-cli-6u.9][3] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.72/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.8/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.9.md

<!-- sase:referenced-by:end -->
