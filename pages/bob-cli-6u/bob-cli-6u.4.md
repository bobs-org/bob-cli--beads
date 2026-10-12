# Bead: bob-cli-6u.4 — Projects sync and capture + use the inline ^prj date

[Bead Pages](../README.md) / [bob-cli-6u](README.md) / bob-cli-6u.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.70](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.70.md) · **Assignee:** `bob-cli-6u.4` · **Size:** medium
**Created:** 2026-10-12 10:25:47 EDT · **Closed:** 2026-10-12 12:13:51 EDT
**Plan:** [202610/prj\_line\_project\_blocking.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_project_blocking.md)

## Description

cli-projects: sync hoists frontmatter scheduled onto ^prj, stops deleting inline ^prj dates, reads propagation/#hide/marker from ^prj, places Sub-projects after Depends-On; capture + writes the date inline; help, docs, and tests.

## Notes

[2026-10-12T14:45:33Z · 72] COORDINATION — bob-cli-6t.2 (project pull-in, §12.10) relies on projects::edits::normalize_task_hide_tag (made pub(crate)) for byte-identical #hide removal (PP22). Its PP23 asserts that after a pull-in, bob projects sync --dry-run reports no change for the project. If it has landed, keep that helper's bytes and visibility. Point DrainState's future-schedule input at ^prj's inline date, and keep PP23 passing after the hoist and the Sub-projects reorder (marker after the Depends-On line). The pull-in's SUBOPEN check reads that marker line. See research:202610/bob_cli_6t_6u_epic_conflict.md.

[2026-10-12T16:06:12Z · bob-cli-6u.4] Live dry-run (BOB_DIR=~/bob projects sync --dry-run): 10 schedules hoisted — sase_back_policy 2026-09-02; sase_better_installs 2026-09-04; sase_better_vars 2026-08-20; sase_blog_0 2026-08-24; sase_bug_bash 2026-09-13; sase_message_boards 2026-10-16 (future); sase_more_agent_clis 2026-07-31; sase_polish_proc_lanes 2026-09-12; sase_skill_bundles 2026-07-29; sase_toobig_symvision 2026-09-24. Vault untouched.

[2026-10-12T16:11:59Z · bob-cli-6u.4] PROPOSED FOLLOW-UP: capture::r#ref percent-listen CLI tests fail identically on clean master (percent_listen_reference_runs_existing_worker_and_installs_audio, failed_percent_listen_worker_keeps_listen_retry_guidance) — tracked by bob-cli-6m

[2026-10-12T16:13:51Z · bob-cli-6u.4] Hoist leftover YAML scheduled onto ^prj (frontmatter wins, terminal/invalid left, dry-run counts hoists), stop deleting inline dates, switch hide/marker/surfacing to ProjectTaskLine.scheduled_date, Sub-projects after Depends-On, capture + writes [scheduled::] on ^prj. native::projects 64/64; CLI projects/capture/freshness/hooks/help green; just all fmt+clippy pass; two baseline capture::r#ref percent-listen failures identical on clean master (bob-cli-6m); live BOB_DIR=~/bob projects sync --dry-run: 10 hoists including future sase_message_boards 2026-10-16, 0 writes; vault untouched; no --epic-symbol leftovers.

## Dependencies

- **Blocks:** [bob-cli-6u.16](bob-cli-6u.16.md) ◐ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.17](bob-cli-6u.17.md) ◐ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.2](bob-cli-6u.2.md) ✓ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.9](bob-cli-6u.9.md) ◐ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.4/README.md) | [bob-cli-6u.4](bob-cli-6u.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`23f2fd9`](https://github.com/bobs-org/bob-cli/commit/23f2fd90e7bade2f6ff5973a6d3e4e6892208a0b) | feat(projects): hoist YAML scheduled onto ^prj and keep inline dates | [bob-cli-6u.4](bob-cli-6u.4.md) | 2026-10-12 12:15:37 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:72][1] | Assess 6u phase state and deps for conflict analysis with 6t | 1 |
| read-by | [agent:bob-cli-6u.8][2] | Need epic and children status | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.72/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.8/README.md

<!-- sase:referenced-by:end -->
