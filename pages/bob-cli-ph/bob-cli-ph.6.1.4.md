# Bead: bob-cli-ph.6.1.4 — Add drawer typing expansion and semantic preview annotations

[Bead Pages](../README.md) / [bob-cli-ph.6.1](bob-cli-ph.6.1.md) / bob-cli-ph.6.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ph.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.6.md) · **Assignee:** `bob-cli-ph.6.1.4` · **Size:** medium
**Created:** 2026-11-25 08:39:53 EST · **Closed:** 2026-11-25 15:49:41 EST
**Plan:** [202611/capture\_true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_true_case_drawers.md)

## Description

drawer-editor-wire: implement expand_drawer_marker through hypothetical parser admission, add marker provenance to drawer objects and drawer annotations to preview header lines, and cover offsets, before/after snapshots, and excluded contexts. Keep Mac keystroke handling and fixture regeneration in bob-cli-ph.8.

## Notes

[2026-11-25T20:49:15Z · bob-cli-ph.6.1.4] PROPOSED FOLLOW-UP: lib baseline failures reproduce on clean tree - capture_complete routes_tasks three_component_marker_keeps_route_and_task_contexts (#requirements vs #"REQUIREMENTS") and task_merge task_drawers_and_project_h2_drawers_resolve_for_merge (expects \t- **REQUIREMENTS** not produced); no tracking bead found

[2026-11-25T20:49:22Z · bob-cli-ph.6.1.4] PROPOSED FOLLOW-UP: 18 CLI failures reproduce identically on clean tree - inbox_route x2, note_pull fixture x3, project_note x3, project_note_offer x6, task_theme_writes, completion drawers_complete_after_id_hash, ref_library today theme, task_status_hooks sync; no tracking bead found

[2026-11-25T20:49:29Z · bob-cli-ph.6.1.4] PROPOSED FOLLOW-UP: just docs-check word-budget errors pre-existing on clean tree - plugin-apis 9276/8000, capture-syntax 6011/6000, hotkeys 6068/6000; json-outputs.md kept at/below 6000 by this phase

[2026-11-25T20:49:41Z · bob-cli-ph.6.1.4] drawer-editor-wire done. RewriteRule::ExpandDrawerMarker expands lone-star (- *) and autopaired (- **|) bullets to **** with caret parked between pairs, admitted only when the editor parser yields a DrawerBullet span for a hypothetical bold title plus nested note (task, note-less, project-note, record, notebook-seed families; route-only/nested/plain/checkbox/blocks-sigil/multiplication/emphasis/template/no-cursor stay literal). DrawerJson gains marker (bold/legacy_caps/section) sourced from selection/creation incl. H2; dry-run and commit agree. BlockLineJson gains drawer:{title,key,marker,empty} on task preview headers (removed=before snapshot, else final); pomodoro/record/section paths unmarked. Tests: 11 rewrite unit + 3 block_diff unit + 5 CLI (rewrite JSON, drawer markers, prj section). Docs: capture rewrite contract + json-outputs; docs-gen rerun. Gates: fmt/lint clean; lib 8168 pass with 2 pre-existing clean-tree failures; CLI 4126 pass with 18 pre-existing clean-tree failures; docs-check matches baseline (2 pre-existing budget errors). Wire: rule expand_drawer_marker, edits insert ***/** at caret, drawer object {title,key,marker,created}, preview line drawer {title,key,marker,empty}. Mac phase (ph.8) owns keystroke handling and fixture regen.

## Dependencies

- **Depends on:** [bob-cli-ph.6.1.3](bob-cli-ph.6.1.3.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-ph.6.1.5](bob-cli-ph.6.1.5.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.6.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.6.1.4/README.md) | [bob-cli-ph.6.1.4](bob-cli-ph.6.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`dfc7fac`](https://github.com/bobs-org/bob-cli/commit/dfc7facb18ded459c5471372a65731a543e5f1f7) | feat(capture): wire drawer editor rewrite markers through JSON and previews | [bob-cli-ph.6.1.4](bob-cli-ph.6.1.4.md) | 2026-11-25 15:51:26 EST |
