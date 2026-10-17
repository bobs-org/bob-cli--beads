# Bead: bob-cli-8w.3 — Portable open plan and URL builder in CaptureCore

[Bead Pages](../README.md) / [bob-cli-8w](README.md) / bob-cli-8w.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.8q](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.8q.md) · **Assignee:** `bob-cli-8w.3` · **Size:** small
**Created:** 2026-10-17 15:54:14 EDT · **Closed:** 2026-10-17 16:44:26 EDT
**Plan:** [202610/ctrl\_enter\_capture\_and\_open.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ctrl_enter_capture_and_open.md)

## Description

mac-open-core: in bob-mac-capture's CaptureCore, decode `open_notes` and add `CaptureOpenPlan`: bob's entries, or a single shared fallback for older bob that replaces the two duplicated heuristics. Add the `bob-open-notes` URL builder and helpers that save the plan into and read it back from notifications, all covered by portable tests.

## Notes

[2026-10-17T20:44:26Z · bob-cli-8w.3] Implemented CaptureCore open_notes decoding, normalized open plan with legacy fallback, bob-open-notes URL builder, and notification payload round trip. Verified just portable-check on athena: 1,312 tests passed; epic-symbol check reports none.

## Dependencies

- **Depends on:** [bob-cli-8w.1](bob-cli-8w.1.md) ✓ · ⧖ 2026-10-17
- **Depends on:** [bob-cli-8w.2](bob-cli-8w.2.md) ✓ · ⧖ 2026-10-17
- **Blocks:** [bob-cli-8w.4](bob-cli-8w.4.md) ◐ · ⧖ 2026-10-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-8w.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8w.3/README.md) | [bob-cli-8w.3](bob-cli-8w.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@a924620`](https://github.com/bobs-org/bob-mac-capture/commit/a924620ae097ab3ce4865cf2c54c16fbc505a9dc) | feat(capture): add portable open plan and URI builder | [bob-cli-8w.3](bob-cli-8w.3.md) | 2026-10-17 16:45:03 EDT |
