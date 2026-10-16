# Bead: bob-cli-84.4 — Panel model Tabs filter, switching, and states

[Bead Pages](../README.md) / [bob-cli-84](README.md) / bob-cli-84.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.7w](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.7w.md) · **Assignee:** `bob-cli-84.4` · **Size:** medium
**Created:** 2026-10-15 17:50:48 EDT · **Closed:** 2026-10-16 07:22:23 EDT
**Plan:** [202610/highlights\_tabs\_switcher.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_tabs_switcher.md)

## Description

tabs-model: RefsPanelModel gains the presentation source, the `tabsFilter` flag, the tabs state, and the tab-row map. It handles ⌘T and ⌘R re-snapshots, the Esc/⌫ ladder, and a ↵ held until the first snapshot lands. Matched rows switch through `openInHighlights` without `recordOpen`; collision and unmatched rows switch through the session's select, with a stale-tab banner. Synthetic rows survive library publications. Preview hooks and model tests use a fake reader.

## Notes

[2026-10-16T11:22:03Z · bob-cli-84.4] PROPOSED FOLLOW-UP: Add the Bob Mac Capture Accessibility read/select boundary decision record — skipped because this epic's DECISIONS set decision_record=no.

[2026-10-16T11:22:09Z · bob-cli-84.4] PROPOSED FOLLOW-UP: Repair Mac test verification — just typecheck-tests reproduces the missing-SDK failure on clean base 94a4e589 (tracked by bob-cli-7o); with an explicit SDK, BobMacCaptureTests also fails on clean base at RefsInspectorTests.swift:483–485 because async results are passed inside XCTest autoclosures. The changed RefsPanelModelTests.swift type-checks; the other three test targets pass.

[2026-10-16T11:22:23Z · bob-cli-84.4] Verified bundle.sh and app compilation on Mac; Athena just portable-check passed 1,236 tests. Explicit-SDK Mac typecheck compiled this phase's tests; the clean-base RefsInspectorTests errors and missing-SDK just typecheck-tests defect are recorded as PROPOSED FOLLOW-UPs.

## Dependencies

- **Depends on:** [bob-cli-84.2](bob-cli-84.2.md) ✓ · ⧖ 2026-10-15
- **Blocks:** [bob-cli-84.5](bob-cli-84.5.md) ✓ · ⧖ 2026-10-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-84.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-84.4/README.md) | [bob-cli-84.4](bob-cli-84.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@a4009a4`](https://github.com/bobs-org/bob-mac-capture/commit/a4009a44760cfe0085e9beb4c174388a73d45261) | feat(refs): add Highlights tabs model and actions | [bob-cli-84.4](bob-cli-84.4.md) | 2026-10-16 07:23:45 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-84.4][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-84.4/README.md

<!-- sase:referenced-by:end -->
