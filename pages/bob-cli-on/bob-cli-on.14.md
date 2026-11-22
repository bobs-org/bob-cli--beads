# Bead: bob-cli-on.14 — Mac bullet indentation beyond two levels

[Bead Pages](../README.md) / [bob-cli-on](README.md) / bob-cli-on.14

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ex](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ex.md) · **Assignee:** `bob-cli-on.14` · **Size:** medium
**Created:** 2026-11-21 11:13:27 EST · **Closed:** 2026-11-22 08:56:17 EST
**Plan:** [202611/task\_requirements.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_requirements.md)

## Description

mac-nesting: generalize Tab/Shift-Tab, Ctrl-J continuation, paste placeholders, and empty-row deletion in Bob Mac Capture from the fixed 0/2-space levels to any authored depth.

## Notes

[2026-11-22T13:56:17Z · bob-cli-on.14] Generalized Mac continuation-bullet indent/outdent, Ctrl-J indent copy, paste placeholders, and empty-row Backspace to any even ASCII-space depth (Tab increase capped at previous row + 2). Decode sub_bullet_depths beyond 2. Verified: just portable-check, Mac scratch typecheck-tests, just docs-check, and Scripts/macos-ci-check (run 45028055861, snapshot fe44d3d) all passed.

## Dependencies

- **Depends on:** [bob-cli-on.13](bob-cli-on.13.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-on.15](bob-cli-on.15.md) ◐ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.14](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.14/README.md) | [bob-cli-on.14](bob-cli-on.14.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.14][1] | Need full description including notes and remaining work after truncated first read | 2 |
| read-by | [agent:bob-cli-on.6.1.land][2] | Check whether the Mac nesting phase covers sub_bullet_depths protocol docs | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.14/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.6.1.land.md

<!-- sase:referenced-by:end -->
