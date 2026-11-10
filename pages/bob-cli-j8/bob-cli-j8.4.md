# Bead: bob-cli-j8.4 — Create notebooks with @parent^id@ %n

[Bead Pages](../README.md) / [bob-cli-j8](README.md) / bob-cli-j8.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3x.linker.w0.md) · **Assignee:** `bob-cli-j8.4` · **Size:** large
**Created:** 2026-11-09 12:11:27 EST · **Closed:** 2026-11-10 00:18:54 EST
**Plan:** [202611/bob\_notebooks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_notebooks.md)

## Description

capture-notebook-create: make `%n` on a `^`-sealed project capture create `<parent>_<id>.md` as a notebook whose summary is the item text, seed notes and ALL-CAPS sections from its bullets, make it visible to later items in the same draft, rewrite the affected catalogs in the same all-or-nothing batch, and fix the stale `%n` sentence tracked by bob-cli-j3.

## Notes

[2026-11-10T05:18:54Z · bob-cli-j8.4] Verified capture-notebook-create on this workspace.

Drafts such as `Neovim config notes @dev^nvim@ %n` parse as NotebookCreate, create `<parent>_<id>.md`, seed notes and ALL-CAPS sections from nested bullets, rewrite owner catalogs in the same capture batch, and make the new route visible to later same-draft items. Parse, preview, and commit agree. GRAMMAR_REVISION is 25.

Verification:
- cargo test --lib capture_language::tests::notebook: 31 passed
- cargo test --test cli capture::notebook_create: 7 passed (create+catalog, seed+later notes, empty-summary refusal, used-before-created, colon `%n` stays pomodoro_note_conflict, notebook seal without `%n` stays notebook_project_seal, area seal without `%n` stays project-note create)
- cargo test --test cli docs_reference: ok after regenerating clap goldens for capture-parse.md and capture-complete.md
- just rustc_gate/clippy with -D unused: green after typing the discover_notebook_creates vec so the DiscoveredNotebookCreate re-export is used
- docs/capture.md picker sentence now documents caret `%n` as notebook create; colon/incomplete/`#name` `%n` remains pomodoro_note_conflict (recorded on bob-cli-j3 without closing it)

just check was not fully green on this tree: native::task_merge::tests::mg18_merge_source_with_descendant_anchor_archives_through_bound_pair fails on clean origin/master as well (dest archive planner uses a `_done` guess instead of the `done_tasks` bound archive). just docs-check fails with a bob-mac-capture mount collision against the authored docs/reference/mac-capture/index.md landing page. Neither is caused by this phase.

PROPOSED FOLLOW-UP: pre-existing mg18 bound-archive vs `_done` guess — native::task_merge::tests::mg18_merge_source_with_descendant_anchor_archives_through_bound_pair expects dest to contain done/custom_archive#^src or #^keep but the planner writes done/src_done; reproduces on clean master with this phase stashed.
PROPOSED FOLLOW-UP: just docs-check bob-mac-capture mount collision — bob-docs errors that mount 'bob-mac-capture' -> 'reference/mac-capture' ships index.md which collides with the committed landing page docs/reference/mac-capture/index.md; docs-gen's bob-docs gen step was skipped for the same reason.

## Dependencies

- **Depends on:** [bob-cli-j8.2](bob-cli-j8.2.md) ✓ · ⧖ 2026-11-09
- **Depends on:** [bob-cli-j8.3](bob-cli-j8.3.md) ✓ · ⧖ 2026-11-09
- **Blocks:** [bob-cli-j8.5](bob-cli-j8.5.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-j8.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-j8.4.md) | [bob-cli-j8.4](bob-cli-j8.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ab021e2`](https://github.com/bobs-org/bob-cli/commit/ab021e2db09c3776d737e9380a236f823bcb42b4) | feat(capture)!: create notebooks from sealed @parent^id@ %n drafts | [bob-cli-j8.4](bob-cli-j8.4.md) | 2026-11-10 00:20:18 EST |
