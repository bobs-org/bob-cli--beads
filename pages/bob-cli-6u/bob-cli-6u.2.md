# Bead: bob-cli-6u.2 — Remove the YAML model and rebuild project reasons from the ^prj line

[Bead Pages](../README.md) / [bob-cli-6u](README.md) / bob-cli-6u.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.70](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.70.md) · **Assignee:** `bob-cli-6u.2` · **Size:** medium
**Created:** 2026-10-12 10:25:46 EDT
**Plan:** [202610/prj\_line\_project\_blocking.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_project_blocking.md)

## Description

cli-model: delete 54a54bf's frontmatter reader, depends_on parse/splice, and target resolution; revert its incidental changes; rebuild ProjectContext and project reasons from the ^prj line; add the #prj_is_blocked line helper.

## Notes

[2026-10-12T14:45:27Z · 72] COORDINATION — bob-cli-6t.2 (project pull-in, running since 10:28 EDT) is editing src/native/projects/scan.rs, mod.rs and edits.rs. It adds a crate-visible drain_state/DrainState that wraps parse_project (open_unhidden_count, unstruck Sub-projects children, the project's future schedule) and makes edits::normalize_task_hide_tag pub(crate). Its reasoning log says it takes §12.10 Rule step 3 from 6s.2's YAML model (project_dependencies::*, frontmatter scheduled/depends_on), because 6s.5 never landed. Before starting, run git log origin/master -- src/native/projects src/native/task_complete. If 6t.2 has landed: revert only the alias helpers from 54a54bf^ (never restore scan.rs wholesale), keep drain_state, and re-point its schedule and project-reason inputs to the ^prj line rather than deleting its callers. See research:202610/bob_cli_6t_6u_epic_conflict.md.

## Dependencies

- **Depends on:** [bob-cli-6u.1](bob-cli-6u.1.md) ✓ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.4](bob-cli-6u.4.md) ◐ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.5](bob-cli-6u.5.md) ◐ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.7](bob-cli-6u.7.md) ◐ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.8](bob-cli-6u.8.md) ◐ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.2/README.md) | [bob-cli-6u.2](bob-cli-6u.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:72][1] | Assess 6u phase state and deps for conflict analysis with 6t | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.72/README.md

<!-- sase:referenced-by:end -->
