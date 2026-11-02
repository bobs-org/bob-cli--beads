# Bead: bob-cli-fc.2 — Several notes on one existing task

[Bead Pages](../README.md) / [bob-cli-fc](README.md) / bob-cli-fc.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.c0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.c0.md) · **Assignee:** `bob-cli-fc.2` · **Size:** medium
**Created:** 2026-11-01 12:53:08 EST · **Closed:** 2026-11-01 17:35:41 EST
**Plan:** [202611/capture\_drawer\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_drawer_bullets.md)

## Description

note-bullets: let a note-less `@route+id` (or `@route+id#drawer`) item file each first-level bullet as its own note, file drawer bullets into the target's drawers, and report notes and drawers in JSON and human output.

## Notes

[2026-11-01T22:35:25Z · bob-cli-fc.2] PROPOSED FOLLOW-UP: Fix pre-existing clippy useless_format denial in tests/cli/capture/keep_moving.rs:263 (&format!("-p"), &format!("{first_n}")); just check fails on clean HEAD (file untouched by fc.2, git diff empty, base has identical lines) with -D clippy::useless-format; no existing task bead tracks it

[2026-11-01T22:35:41Z · bob-cli-fc.2] Implemented note-bullets multi-note: execution/editor parse accept note-less @route+id with first-level bullets (existing targets under-task for drawer bullets, glued drawer drops DrawerText when notes exist, multi_note_marker for s/$/%c/--clip, empty_drawer_bullet for existing-drawer childless); writer plans each note/drawer group via plan_sub_bullet_capture/plan_prj_section_capture in draft order with atomic rollback, tracks notes/drawers/item-drawer per contract; output adds notes/drawers JSON and draft-order human with new-drawer tags; docs updated (capture.md Several-notes subsection + grammar rows + JSON fields, json-outputs notes/drawers + multi_note_marker code, capture --help paragraph) with docs-gen/docs-check green; tests: 12/12 note_bullets pass (worked example byte-for-byte + JSON/human, logs insertion, merge, childless/reserved refusals, glued, same-line nest/position, retype, & owner, markers, rollback) plus 7/7 drawer_bullets green; just check blocked only by pre-existing keep_moving.rs useless_format (recorded as PROPOSED FOLLOW-UP, file untouched)

## Dependencies

- **Depends on:** [bob-cli-fc.1](bob-cli-fc.1.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-fc.3](bob-cli-fc.3.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-fc.4](bob-cli-fc.4.md) ◐ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fc.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fc.2/README.md) | [bob-cli-fc.2](bob-cli-fc.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`5ac2fbc`](https://github.com/bobs-org/bob-cli/commit/5ac2fbc223ae01e6e4554edf0ddf1485e077eddd) | feat(capture): several notes on one existing task | [bob-cli-fc.2](bob-cli-fc.2.md) | 2026-11-01 18:46:17 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fc.2][1] | check full scope and notes | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fc.2/README.md

<!-- sase:referenced-by:end -->
