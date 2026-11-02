# Bead: bob-cli-fc.3 — Bullet drawer menu, docs, and memory records

[Bead Pages](../README.md) / [bob-cli-fc](README.md) / bob-cli-fc.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.c0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.c0.md) · **Assignee:** `bob-cli-fc.3` · **Size:** medium
**Created:** 2026-11-01 12:53:08 EST · **Closed:** 2026-11-01 20:53:14 EST
**Plan:** [202611/capture\_drawer\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_drawer_bullets.md)

## Description

bullet-menu: open the drawer completion menu at a first-level bullet's `#`, replace with the bare ALL-CAPS title (plus the optional nested-bullet continuation), finish the docs, and write the accepted memory records.

## Notes

[2026-11-02T01:31:42Z · bob-cli-fc.3] PROPOSED FOLLOW-UP: Fix 5 pre-existing cargo test --test cli failures that reproduce identically on the clean base tree (git stash verified): capture::pomodoro_link::capture_named_pomodoro_updates_both_notes_and_skips_current, capture_named_pomodoro_dry_run_and_failures_leave_notes_untouched, capture::project_note::capture_project_note_task_links_write_the_worked_example, capture::project_note_offer::offer_named_pomodoro_is_created_only_when_a_pick_lands_there, capture::task_theme_writes::named_capture_writes_a_type_without_a_shown_suggestion — named-Pomodoro link/project-note captures no longer write the expected [type:: NAME] field on the linked task line.

[2026-11-02T01:31:51Z · bob-cli-fc.3] PROPOSED FOLLOW-UP: Third-level authored bullet grammar — drawer notes filed through a drawer bullet (and the bullet drawer menu continuation) are one line each under the two-level authored grammar (AuthoredDepth has about 80 uses across 12 files); a third authored level would let drawer notes carry detail bullets.

[2026-11-02T01:53:14Z · bob-cli-fc.3] Bullet drawer menu landed: capture-complete opens context drawer at a first-level bullet's # (existing task, ^prj, new task, new project note), rows insert the bare ALL-CAPS title with the optional \n  - continuation, other positions return an empty success, nested # still types. Fixed a multi-note commit disagreement (eager new-task drawer resolution refused ^prj section titles with the wrong scope) found by the accept-and-commit agreement test, which passes for all four target kinds. Docs (capture.md, completion.md, json-outputs.md, capture-complete --help) regenerated; just docs-gen/docs-check pass. Memory: decisions:capture-bullets-mirror-the-task-block added, capture-sigils-say-where-what-how marked superseded-in-part, glossary:task-drawer updated, sase memory init run. just check: fmt+clippy pass, 4365 lib tests pass, cli tests 2709 pass with the same 5 pre-existing failures that reproduce on the clean base tree (recorded as PROPOSED FOLLOW-UP). Shell completion is single-line only so it never reaches a bullet start (documented and tested).

## Dependencies

- **Depends on:** [bob-cli-fc.2](bob-cli-fc.2.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-fc.4](bob-cli-fc.4.md) ✓ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fc.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fc.3/README.md) | [bob-cli-fc.3](bob-cli-fc.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`971d864`](https://github.com/bobs-org/bob-cli/commit/971d864f6c8ca91ed78f01aca41c0f4d93643efa) | feat(capture): bullet drawer completion menu, docs, and memory records | [bob-cli-fc.3](bob-cli-fc.3.md) | 2026-11-01 20:54:25 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fc.3][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fc.3/README.md

<!-- sase:referenced-by:end -->
