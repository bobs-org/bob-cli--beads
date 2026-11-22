# Bead: bob-cli-on.10.1.5 — Nav and Block ID Prompt requirement guards and the owner Task Card

[Bead Pages](../README.md) / [bob-cli-on.10.1](bob-cli-on.10.1.md) / bob-cli-on.10.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.10.md) · **Assignee:** `bob-cli-on.10.1.5` · **Size:** medium
**Created:** 2026-11-21 14:10:17 EST · **Closed:** 2026-11-21 19:36:25 EST
**Plan:** [202611/obsidian\_req\_gestures.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_req_gestures.md)

## Description

nav-guards-and-owner-card: refuse Alt+N, Alt+F, Ctrl+Alt+F, their counted forms, and the other nav task gestures on req lines with the lane copy, redirect Ctrl+Shift+P (and the Task Card stage shortcuts) to the owner's Task Card, and guard Block ID Prompt's Ctrl+Shift+Enter so a req line or carried stub is never linked or unlinked.

## Notes

[2026-11-22T00:36:11Z · bob-cli-on.10.1.5] PROPOSED FOLLOW-UP: bob-cli origin/master docs-check contract registry tests fail independently of this phase (tools/docs/tests/test_contracts.py expects 54 contracts / README table SHA 34f4f8a4; registry now has 55 including task-requirements.md and walks.md). Reproduced with pytest on the docs-check bob-cli cache at 7cc9493 with no plugin-docs mount. plugin-apis.md is also over the develop/ 8000-word cap (8308) as a warning.

[2026-11-22T00:36:25Z · bob-cli-on.10.1.5] Nav 2.103.0 and Block ID Prompt 1.42.0: req-line guards refuse Alt+N, Alt+F, Ctrl+Alt+F (and counted forms), Alt+P, and Ctrl+Shift+M with the lane/carried copy and write nothing; Ctrl+Shift+P and Task Card stage chords open the owner card (depth-1/3, excluded, carried stub); Ctrl+Shift+Enter refuses req/stub lines before task-link mode. scripts/test-navigation-req-guards.cjs and scripts/test-block-id-prompt-req-guard.cjs 23/23; npm test 8516 pass / 4 skip + 13 perf; docs:gen + docs:check lint/build/URLs passed (bob-cli contract-registry snapshot tests fail on origin/master independently; noted as PROPOSED FOLLOW-UP). 550 stayed 998 lines. Synced both plugins to the vault (block-id via proving ancestor 39563684 then descendant 235c7db, no -F).

## Dependencies

- **Depends on:** [bob-cli-on.10.1.2](bob-cli-on.10.1.2.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-on.10.1.6](bob-cli-on.10.1.6.md) ◐ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.10.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.5/README.md) | [bob-cli-on.10.1.5](bob-cli-on.10.1.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.10.1.5][1] | Need remaining notes, design file, DECISIONS, and whether earlier work landed | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.5/README.md

<!-- sase:referenced-by:end -->
