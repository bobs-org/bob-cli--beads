# Bead: bob-cli-ey.5 — Bob Mac Capture drawer menu and drawer previews

[Bead Pages](../README.md) / [bob-cli-ey](README.md) / bob-cli-ey.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2x.linker.w0.md) · **Assignee:** `bob-cli-ey.5` · **Size:** medium
**Created:** 2026-10-31 12:52:04 EDT · **Closed:** 2026-11-01 03:25:55 EST
**Plan:** [202610/capture\_drawers\_and\_directives.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_drawers_and_directives.md)

## Description

mac-drawers: render the `drawer` context with On this task and Recent groups, the New drawer row, refused rows, and bob's per-row consequence footer; style `drawer` spans; show the "new drawer" and retype rows in previews; require `grammar >= 3`; delete `task_section` rendering; regenerate fixtures; update the Mac docs.

## Notes

[2026-11-01T08:25:05Z · bob-cli-ey.5] PROPOSED FOLLOW-UP: bob capture-complete drawer menu emits only the target task rows (group "drawers", empty detail) at bob-cli e660c8d8 -- no recent/new groups, no detail/consequence/refused, no initial_selection none for @route+id#, and replacement starts after the # instead of covering it. DrawerCandidate already has group/note_count/last_seen/detail/creates/refused/consequence/cursor_after but candidates.rs drawer_candidates fills only the task rows, and engine.rs initial_selection() returns early because result.query is None for drawers. Plan sec3.6 defines the full menu. The Mac renders every one of those fields when present (drawer-contract-complete-* are synthetic overlays); regenerate with Scripts/generate-drawer-fixtures.sh once Bob emits them, the README gap list empties itself.

[2026-11-01T08:25:11Z · bob-cli-ey.5] PROPOSED FOLLOW-UP: bob capture --format json sub_bullet items carry only the legacy parent_section string, not the per-item drawer {title, key, created} object plan sec3.3/sec3.7 call for, so the Mac cannot show the new-drawer capsule against a real bob yet (it decodes drawer and falls back to parent_section). Also capture-parse drawer spans carry no title/key.

[2026-11-01T08:25:17Z · bob-cli-ey.5] PROPOSED FOLLOW-UP: a separate #type beside a glued drawer (Text @foo+bar#requirements #fix) is not honored at bob-cli e660c8d8: capture-parse reports diagnostic type_marker_not_applicable ("this capture adds a child bullet") and capture --dry-run returns no task_theme, although the epic goal says the drawer capture optionally retypes the task in the same transaction. The Mac preview already renders the Type row beneath the drawer header when task_theme is present (drawer-contract-capture-new-retype.json).

[2026-11-01T08:25:23Z · bob-cli-ey.5] PROPOSED FOLLOW-UP: Scripts/macos-ci-check (docs/develop/ci.md) pushes a throwaway branch to GitHub, which this agent did not run unprompted, and the Mac was offline for ssh. BobMacCapture/BobMacCaptureTests changes (CaptureDrawerMenuView, drawerMenuPresentation, CaptureDrawerMenuHostedTests, CapturePanelModelTests drawer cases, grammar-3 gate hosted tests) are unverified on macOS: run just typecheck-tests/swift test there or macos-ci-check before relying on them.

[2026-11-01T08:25:48Z · bob-cli-ey.5] PROPOSED FOLLOW-UP: Scripts/generate-task-type-fixtures.sh still drives the retired attached forms (@route+id#type, @route^id#type); against grammar-3 bob, regenerating changes 21 task-type-* fixtures beyond grammar (attached-new/attached-toggle/empty/history now parse as errors or drawer/pomodoro_name contexts). This phase regenerated only task-type-{parse,complete}-incomplete-marker.json (grammar 2->3, needed because fake-bob serves the former through the new gate); the rest stay as grammar-2 history and CaptureTaskTypeTests still decode them. Migrate the generator inputs to separate-token #type and drop the attached cases.

[2026-11-01T08:25:55Z · bob-cli-ey.5] Mac drawer menu and previews implemented in bob-mac-capture: drawer completion context (CaptureDrawerMenuPresentation + CaptureDrawerMenuView with On this task / Recent groups, dashed New drawer row, refused rows as no-ops, Bob consequence footer, unselected open), drawer span color family, new-drawer capsule + Type row in sub-bullet previews, task_section rendering/childCount items deleted, grammar gate raised to 3, directive + incomplete-marker fixtures regenerated from bob e660c8d8, Scripts/generate-drawer-fixtures.sh (real fixtures + labeled synthetic contract overlays for fields bob does not emit yet), fake-bob moved to grammar 3 + drawer fixtures, docs updated. Verified: swift build --build-tests and swift test on athena (Linux, 1898 tests, 0 failures); swift format lint clean on changed lines; docs-check passed through bob-cli; script tests pass; git grep for task_section/task section clean (remaining childCount is the Pomodoro/task child_count field). NOT verified: BobMacCapture/BobMacCaptureTests targets on macOS (Mac offline over ssh; Scripts/macos-ci-check not run because it pushes a branch). bob-cli e660c8d8 does not yet emit Recent/New/refused/consequence rows, initial_selection none for drawers, the drawer capture object, or drawer+#type retype; recorded as PROPOSED FOLLOW-UP notes.

## Dependencies

- **Depends on:** [bob-cli-ey.2](bob-cli-ey.2.md) ✓ · ⧖ 2026-10-31
- **Depends on:** [bob-cli-ey.3](bob-cli-ey.3.md) ✓ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ey.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ey.5/README.md) | [bob-cli-ey.5](bob-cli-ey.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@9a1876d`](https://github.com/bobs-org/bob-mac-capture/commit/9a1876d88223352f4ec8e440dd6b2df6dcc20b25) | feat(mac-capture)!: add the drawer menu and drawer previews, require grammar 3 | [bob-cli-ey.5](bob-cli-ey.5.md) | 2026-11-01 03:35:07 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ey.5][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ey.5/README.md

<!-- sase:referenced-by:end -->
