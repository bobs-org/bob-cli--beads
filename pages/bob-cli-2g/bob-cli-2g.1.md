# Bead: bob-cli-2g.1 — Fuzzy matcher and picker presentation engine (CaptureCore)

[Bead Pages](../README.md) / [bob-cli-2g](README.md) / bob-cli-2g.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-2f.3.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-2f.3.w1.md) · **Assignee:** `bob-cli-2g.1` · **Size:** medium
**Created:** 2026-09-28 18:28:11 EDT · **Closed:** 2026-09-28 18:43:47 EDT
**Plan:** [202609/mac\_active\_task\_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/mac_active_task_picker.md)

## Description

core: add a pure, Foundation-only fuzzy matcher, the task display-text parser for code spans and wikilinks, and the grouped/filtered picker presentation with navigation helpers. Ship thorough CaptureCore unit tests; the app's behavior does not change.

## Notes

[2026-09-28T22:43:37Z · bob-cli-2g.1] PROPOSED FOLLOW-UP: run just format-lint build test on mac (or macOS 26 SwiftPM CI) for the new CaptureCore files — tailnet mac was unreachable (ssh port 22 timeout) during this phase, and no Swift toolchain exists on the Linux host

[2026-09-28T22:43:47Z · bob-cli-2g.1] Implemented FuzzyMatcher, ActiveTaskDisplayText, ActiveTaskPickerPresentation + 3 XCTest suites in bob-mac-capture (6 new files, no app changes). Verified scoring/ranking with an independent Python model of the DP (sudo/later/bob/fix/deep/cafe/q-weight/caret/tie orders all hold); mac host unreachable so just format-lint build test is recorded as follow-up, tests not yet run.

## Dependencies

- **Blocks:** [bob-cli-2g.2](bob-cli-2g.2.md) ◐ · ⧖ 2026-09-28
- **Blocks:** [bob-cli-2g.3](bob-cli-2g.3.md) ◐ · ⧖ 2026-09-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2g.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2g.1/README.md) | [bob-cli-2g.1](bob-cli-2g.1.md) | 0 |
