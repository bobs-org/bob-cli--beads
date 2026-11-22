# Bead: bob-cli-on.15.1.2 — Stage requirement verdicts and preserve branch identity

[Bead Pages](../README.md) / [bob-cli-on.15.1](bob-cli-on.15.1.md) / bob-cli-on.15.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.15](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.15.md) · **Assignee:** `bob-cli-on.15.1.2` · **Size:** medium
**Created:** 2026-11-22 14:56:48 EST · **Closed:** 2026-11-22 16:08:09 EST
**Plan:** [202611/mac\_requirement\_close\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_requirement_close_card.md)

## Description

outcomes: extend the portable Pull-In outcomes and the choice model with typed requirement rows, Met/Drop/Carry/Carry-and-pull verdicts, overlap refusal, branch folding, owner grouping, navigation-only pins, refresh, and commit projections. Follow the outcomes section and test its transition matrix, including default-Met commits and Shift-Return downgrading.

## Notes

[2026-11-22T21:08:09Z · bob-cli-on.15.1.2] Outcomes staged: typed requirement rows (Met/Drop/Carry/Carry-and-pull), component-wise overlap refusal both orders, fold with nested go-with-it, owner grouping with requirements-first sections, nav-only pin, exact-key refresh with branch revalidation, semantic summary excluding folded descendants, all-default committable, Return never pulls requirement, Shift-Return downgrades carry-pulled and selects no pull-ins. Tests: 11 new CapturePullInRequirementOutcomesTests pass; full portable suite 2696 pass, 1 skipped, 0 fail. Format lint warnings only, exit 0. macOS AppKit/SwiftUI targets unverified on Linux (no Xcode); scratch-Mac build and exact-SHA macOS CI deferred to integration phase per plan.

## Dependencies

- **Depends on:** [bob-cli-on.15.1.1](bob-cli-on.15.1.1.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-on.15.1.3](bob-cli-on.15.1.3.md) ◐ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.15.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.15.1.2/README.md) | [bob-cli-on.15.1.2](bob-cli-on.15.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@bab5e5c`](https://github.com/bobs-org/bob-mac-capture/commit/bab5e5cc1074950a7b20b49914afe66104e114f6) | feat(capture): stage requirement verdicts and preserve branch identity | [bob-cli-on.15.1.2](bob-cli-on.15.1.2.md) | 2026-11-22 16:09:21 EST |
