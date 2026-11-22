# Bead: bob-cli-on.6 — Capture grammar, spans, typing rewrite, and NOTES routing for requirements

[Bead Pages](../README.md) / [bob-cli-on](README.md) / bob-cli-on.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ex](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ex.md) · **Assignee:** `bob-cli-on.6` · **Size:** large
**Created:** 2026-11-21 11:13:26 EST · **Closed:** 2026-11-22 07:12:59 EST
**Plan:** [202611/task\_requirements.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_requirements.md)

## Description

capture-reqs: admit requirement bullets at every eligible capture position and depth, add refusals, the req_marker span, the expand_req_marker rewrite, NOTES routing with the first-requirement scoop, and nested requirements in project-note capture; grammar revision 29.

## Notes

[2026-11-22T12:13:15Z · bob-cli-on.6.1.land] PHASE VERIFIED (bob-cli-on.6.1 land agent): the host closed this phase automatically when its child epic bob-cli-on.6.1 closed. I checked each part of the description against master plus this landing.
- Requirement bullets at every eligible position and depth: 7cc94933, plus this landing's level-3+ lexical-helper parity.
- Refusals: req_in_drawer, req_parent, req_state, and req_depth (7cc94933); req_link (3ce97d73).
- req_marker span with depth, and capture grammar 29: capture-parse reports grammar 29.
- expand_req_marker rewrite: c05deef2.
- NOTES routing with the first-requirement scoop: 0a623b70 and 3ce97d73.
- Nested requirements in project-note capture: 0a623b70; the sealed_project_notes_take_requirements_under_task_rows and reqs_new project-row tests pass in just check.
just check passed (lib 7819, cli 3991). Details are in the bob-cli-on.6.1 close note. bob-cli-on itself stays with its own land agent.

## Dependencies

- **Blocks:** [bob-cli-on.13](bob-cli-on.13.md) ◐ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-on.3](bob-cli-on.3.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-on.8](bob-cli-on.8.md) ◐ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.6.md) | [bob-cli-on.6](bob-cli-on.6.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.6.1.2][1] | decisions | 1 |
| read-by | [agent:bob-cli-on.6.1.3][2] | Need parent capture-reqs DECISIONS | 1 |
| read-by | [agent:bob-cli-on.6.1.4][3] | Need the capture-reqs phase authority and its inherited decisions | 1 |
| read-by | [agent:bob-cli-on.6.1.5][4] | Need the parent phase's scope, decisions, and any recorded remainder | 1 |
| read-by | [agent:bob-cli-on.6.1.land][5] | Confirm the phase closed after its child epic landed | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.4/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.5/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.6.1.land.md

<!-- sase:referenced-by:end -->
