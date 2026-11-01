# Bead: bob-cli-fc.1 — Drawer bullets in the capture grammar

[Bead Pages](../README.md) / [bob-cli-fc](README.md) / bob-cli-fc.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.c0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.c0.md) · **Assignee:** `bob-cli-fc.1` · **Size:** medium
**Created:** 2026-11-01 12:53:08 EST · **Closed:** 2026-11-01 14:37:21 EST
**Plan:** [202611/capture\_drawer\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_drawer_bullets.md)

## Description

drawer-bullets: make a first-level bullet's leading `#` a drawer shortcut instead of a type marker, recognize drawer bullets on new tasks and new project notes, render and merge them through the commit resolver, report them in capture-parse, and bump the grammar to 4.

## Notes

[2026-11-01T19:36:53Z · bob-cli-fc.1] PROPOSED FOLLOW-UP: third-level authored bullet grammar so drawer notes can carry nested details (plan non-goal; AuthoredDepth stays two levels)

[2026-11-01T19:37:21Z · bob-cli-fc.1] Grammar 4 first-level drawer shortcuts on new tasks and new project notes. Verified: just check, just docs-check, just docs-gen; unit tests in capture_language::tests::drawer_bullet; CLI tests in tests/cli/capture/drawer_bullets.rs (catalog spelling, merge, reserved/empty/text, same-line position, childless NYC, project-note ## Future Work); type-marker first-level skip with nested  - #fix still typing. No --epic-symbol leftovers. Memory writes left to phase bullet-menu.

## Dependencies

- **Blocks:** [bob-cli-fc.2](bob-cli-fc.2.md) ✓ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fc.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fc.1/README.md) | [bob-cli-fc.1](bob-cli-fc.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bbd26d9`](https://github.com/bobs-org/bob-cli/commit/bbd26d97ccf24217b20896c8275f4f5bbaa67ce2) | feat(capture)!: first-level \`- #…\` is a drawer shortcut (grammar 4) | [bob-cli-fc.1](bob-cli-fc.1.md) | 2026-11-01 15:29:36 EST |
| bob-cli | [`f490d88`](https://github.com/bobs-org/bob-cli/commit/f490d88f2d6ce87e5b05cf6aec2a5b46fdcb22de) | fix(capture): keep agenda clippy, goldens, and gcal checks green | [bob-cli-fc.1](bob-cli-fc.1.md) | 2026-11-01 15:31:38 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fc.1][1] | Confirm closed status before final declaration | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fc.1/README.md

<!-- sase:referenced-by:end -->
