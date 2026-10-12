# Bead: bob-cli-6u.7 — Close and recovery paths respect project blocking and write \[unblocked::\]

[Bead Pages](../README.md) / [bob-cli-6u](README.md) / bob-cli-6u.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.70](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.70.md) · **Assignee:** `bob-cli-6u.7` · **Size:** medium
**Created:** 2026-10-12 10:25:59 EDT · **Closed:** 2026-10-12 11:49:03 EDT
**Plan:** [202610/prj\_line\_project\_blocking.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_project_blocking.md)

## Description

cli-close: StillBlockedProject verdict, residents recover with their ^prj (tag stripped), Ready recoveries write [unblocked::], recovery parity, PDC and UB close tests.

## Notes

[2026-10-12T14:45:38Z · 72] COORDINATION — bob-cli-6t.2 (project pull-in, §12.10, running) adds task_complete/project_pull_in.rs and wires it into plan_successors. The wiring relaxes the [id::] gate and lets a pull-in verdict replace Recover("project_task") for an emptied project's ^prj. It adds trigger/hide_removed to UnblockedRow and StillBlockedRow and a surfaced verb in capture/output.rs. It was planned to build on 6s.5's project verdict, which never landed; this phase now owns that verdict. Whichever lands second must merge, not overwrite:
(1) StillBlockedProject applies to residents only. ^prj has only its own reasons (Design §2), which §12.10 steps 1–2 already cover.
(2) The project_member cascade must fire whenever ^prj recovers, including when the pull-in verdict replaced the project_task row. An emptied N can still hold [?] residents tagged #hide, because §12.10's REMAINING skips #hide lines.
(3) The pull-in's recover-rank path (? → space) writes [unblocked::] through mark_unblocked like every other Ready recovery. The linked ? → * path skips it.
(4) successors.rs is 1488 lines and both plans say to put new logic in new modules.
See research:202610/bob_cli_6t_6u_epic_conflict.md.

[2026-10-12T15:48:49Z · bob-cli-6u.7] PROPOSED FOLLOW-UP: cli capture::r#ref listen-worker tests fail on clean base too (missing listen fixture dir) — failed_percent_listen_worker_keeps_listen_retry_guidance, percent_listen_reference_runs_existing_worker_and_installs_audio

[2026-10-12T15:49:03Z · bob-cli-6u.7] cli-close done: StillBlockedProject verdict + project_member cascade (outside breaker) in successors.rs via new task_complete/project_close module, parity in recovery.rs, [unblocked::] on Ready recoveries with tag strip, project path in still_blocked JSON/human output. Verified: cargo fmt/clippy clean, lib 2406 passed, new PDC1-3 + UB1-4/UB6 successor tests, recovery PDC tests, CLI project_close tests, prefilter line-model case all pass; 2 r#ref listen failures reproduce on clean base (noted as follow-up)

## Dependencies

- **Blocks:** [bob-cli-6u.16](bob-cli-6u.16.md) ◐ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.17](bob-cli-6u.17.md) ◐ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.2](bob-cli-6u.2.md) ✓ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.3](bob-cli-6u.3.md) ✓ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.7/README.md) | [bob-cli-6u.7](bob-cli-6u.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`13d183f`](https://github.com/bobs-org/bob-cli/commit/13d183ff74594ae691034c83ce43d2d5b21d3f80) | feat(task-complete): respect project blocking in close paths | [bob-cli-6u.7](bob-cli-6u.7.md) | 2026-10-12 11:50:31 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:72][1] | Assess 6u phase state and deps for conflict analysis with 6t | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.72/README.md

<!-- sase:referenced-by:end -->
