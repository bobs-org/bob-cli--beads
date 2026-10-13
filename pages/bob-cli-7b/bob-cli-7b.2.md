# Bead: bob-cli-7b.2 — Toggle, Ensure Next, and link-then-close adopt the drop

[Bead Pages](../README.md) / [bob-cli-7b](README.md) / bob-cli-7b.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.7c.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.7c.w0.md) · **Assignee:** `bob-cli-7b.2` · **Size:** medium
**Created:** 2026-10-13 08:12:08 EDT · **Closed:** 2026-10-13 10:13:07 EDT
**Plan:** [202610/capture\_link\_drops\_blocking\_deps.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_link_drops_blocking_deps.md)

## Description

cli-gestures: route `@route+id!`, `@route+id[#name]`, and `@route:id=x…` through the shared guard helper, print the drop line in their human output, and convert their PDG1 tests into drop tests plus refused-drop consumption tests.

## Notes

[2026-10-13T14:12:50Z · bob-cli-7b.2] PROPOSED FOLLOW-UP: capture::r#ref listen-worker tests fail identically on clean base (environmental, no audio worker in sandbox)

[2026-10-13T14:13:07Z · bob-cli-7b.2] Toggle (@route+id!), Ensure Next (@route+id[#name]), and link-then-close (@route:id=x) now route through resolve_link_guard: eligible own-dependency drops are staged in the batch planner before plan_task_link, with dropped_dependencies + dependency_dropped task_blocks in JSON and the dim drop line in human output (incl. close/reset printers); refused drops keep consumption with drop_refused codes. Removed the now-unused assess_link_target_legacy shim. Converted the 3 PDG1 tests into PDG19 drop tests plus PDG23/PDG24 refused-drop tests (9/9 incl. neighbors pass); fmt+clippy clean; full suite green except 2 pre-existing r#ref listen-worker failures that reproduce identically on the clean base (recorded as follow-up).

## Dependencies

- **Depends on:** [bob-cli-7b.1](bob-cli-7b.1.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-7b.4](bob-cli-7b.4.md) ✓ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7b.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7b.2/README.md) | [bob-cli-7b.2](bob-cli-7b.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bdfc8c3`](https://github.com/bobs-org/bob-cli/commit/bdfc8c3ee3edb5eef6f3ba0dddc12c36ef8095ec) | feat(capture): route toggle, ensure-next and link-then-close through shared link guard | [bob-cli-7b.2](bob-cli-7b.2.md) | 2026-10-13 10:14:59 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7b.2][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-7b.3][2] | Check whether cli-gestures landed so close/toggle JSON fixtures can be generated | 1 |
| read-by | [agent:bob-cli-7b.4][3] | Need cli-gestures close note for evidence commits | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7b.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7b.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7b.4/README.md

<!-- sase:referenced-by:end -->
