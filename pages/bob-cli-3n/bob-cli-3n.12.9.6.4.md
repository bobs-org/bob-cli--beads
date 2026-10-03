# Bead: bob-cli-3n.12.9.6.4 — Apply R9 to label-only lines in the hooks and bring the touched files under size

[Bead Pages](../README.md) / [bob-cli-3n.12.9.6](bob-cli-3n.12.9.6.md) / bob-cli-3n.12.9.6.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-3n.12.9.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-3n.12.9.land.md) · **Assignee:** `bob-cli-3n.12.9.6.4` · **Size:** small
**Created:** 2026-10-03 02:54:24 EDT · **Closed:** 2026-10-03 03:06:39 EDT
**Plan:** [202610/task\_dep\_links\_landing\_remaining.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_dep_links_landing_remaining.md)

## Description

hooks-r9-split: stop the hooks re-adopting a label-only Depends-On line (R9/DW5/DR16), pin it with an adoptable-id test, correct the DW3/DW6 comments, and bring reconcile.rs and dependency_lines.rs back under about 1500 lines.

## Notes

[2026-10-03T07:06:39Z · bob-cli-3n.12.9.6.4] R9 fix verified: plan_empty now deletes a label-only line plus field with no legacy children whatever the field holds; new adoptable-id test fails pre-fix (no line_removed, re-adopts) and passes post-fix; ghost-id case kept. DW3/DW6 comments point at nav writer tests. reconcile.rs 1531->1494 lines, dependency_lines.rs 1580->1304 with DW/summary tests in new dependency_line_writes.rs (341). just all green: 870 CLI + 1561 lib tests, 0 failures. No doc wording change needed (task-status-hooks.md already states R9). No epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-3n.12.9.6.5](bob-cli-3n.12.9.6.5.md) ✓ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3n.12.9.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.12.9.6.4/README.md) | [bob-cli-3n.12.9.6.4](bob-cli-3n.12.9.6.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`94131c7`](https://github.com/bobs-org/bob-cli/commit/94131c7b044a635e53d992ce0fb4f71eb659da6c) | fix(task-status-hooks): R9 label-only Depends-On line deletes line and field | [bob-cli-3n.12.9.6.4](bob-cli-3n.12.9.6.4.md) | 2026-10-03 03:07:44 EDT |
