# Bead: bob-cli-a8.1 — Ctrl+Tab panel switch with preserved state

[Bead Pages](../README.md) / [bob-cli-a8](README.md) / bob-cli-a8.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.9q` · **Assignee:** `bob-cli-a8.1` · **Size:** medium
**Created:** 2026-10-20 15:55:13 EDT · **Closed:** 2026-10-20 18:03:11 EDT
**Plan:** [202610/mac\_capture\_panel\_switch\_and\_perf.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/mac_capture_panel_switch_and_perf.md)

## Description

panel_switch: add the coordinator switch, Ctrl+Tab routing in both panels with a deferred hop, the Refs panelSwitch presentation source, round-trip state tests, switch signposts, and the keyboard/refs/capture docs.

## Notes

[2026-10-20T22:02:54Z · bob-cli-a8.1] PROPOSED FOLLOW-UP: docs-check has 2 pre-existing template-test failures (test_templates_in_material, test_component_chips_in_material) from missing mkdocs github-callouts module; reproduces identically on clean base tree

[2026-10-20T22:03:11Z · bob-cli-a8.1] Implemented panel_switch in bob-mac-capture: BobPanel + switchPanels, RefsPresentationSource.panelSwitch (keep semantics), Ctrl+Tab routing in both panels with deferred hop, AppDelegate.switchPanels with panel-switch signposts, keyboard/refs/capture-panel/diagnostics docs, and router/coordinator/model/controller tests. Verified: portable-check 1472 tests pass, Mac bundle.sh + typecheck-tests PASS, docs-check 2 template failures reproduce identically on clean base (recorded as follow-up).

## Dependencies

- **Blocks:** [bob-cli-a8.2](bob-cli-a8.2.md) ◐ · ⧖ 2026-10-20
- **Blocks:** [bob-cli-a8.3](bob-cli-a8.3.md) ◐ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-a8.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-a8.1/README.md) | [bob-cli-a8.1](bob-cli-a8.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@e99cec6`](https://github.com/bobs-org/bob-mac-capture/commit/e99cec6f7d35e78d07bad679b607aea54b3e6bd9) | feat(capture): add Ctrl+Tab panel switch with preserved state | [bob-cli-a8.1](bob-cli-a8.1.md) | 2026-10-20 18:04:17 EDT |
