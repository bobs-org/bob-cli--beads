# Bead: bob-cli-6u.4 — Projects sync and capture + use the inline ^prj date

[Bead Pages](../README.md) / [bob-cli-6u](README.md) / bob-cli-6u.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.70](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.70.md) · **Assignee:** `bob-cli-6u.4` · **Size:** medium
**Created:** 2026-10-12 10:25:47 EDT
**Plan:** [202610/prj\_line\_project\_blocking.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_project_blocking.md)

## Description

cli-projects: sync hoists frontmatter scheduled onto ^prj, stops deleting inline ^prj dates, reads propagation/#hide/marker from ^prj, places Sub-projects after Depends-On; capture + writes the date inline; help, docs, and tests.

## Notes

[2026-10-12T14:45:33Z · 72] COORDINATION — bob-cli-6t.2 (project pull-in, §12.10) relies on projects::edits::normalize_task_hide_tag (made pub(crate)) for byte-identical #hide removal (PP22). Its PP23 asserts that after a pull-in, bob projects sync --dry-run reports no change for the project. If it has landed, keep that helper's bytes and visibility. Point DrainState's future-schedule input at ^prj's inline date, and keep PP23 passing after the hoist and the Sub-projects reorder (marker after the Depends-On line). The pull-in's SUBOPEN check reads that marker line. See research:202610/bob_cli_6t_6u_epic_conflict.md.

## Dependencies

- **Blocks:** [bob-cli-6u.16](bob-cli-6u.16.md) ◐ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.17](bob-cli-6u.17.md) ◐ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.2](bob-cli-6u.2.md) ✓ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.9](bob-cli-6u.9.md) ◐ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.4/README.md) | [bob-cli-6u.4](bob-cli-6u.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:72][1] | Assess 6u phase state and deps for conflict analysis with 6t | 1 |
| read-by | [agent:bob-cli-6u.8][2] | Need epic and children status | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.72/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.8/README.md

<!-- sase:referenced-by:end -->
