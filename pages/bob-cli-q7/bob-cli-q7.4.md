# Bead: bob-cli-q7.4 — Mac: Go To destination card and Return dispatch

[Bead Pages](../README.md) / [bob-cli-q7](README.md) / bob-cli-q7.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1g6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1g6.md) · **Assignee:** `bob-cli-q7.4` · **Size:** medium
**Created:** 2026-11-25 15:25:24 EST · **Closed:** 2026-11-25 19:47:00 EST
**Plan:** [202611/caret\_address\_goto\_capture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/caret_address_goto_capture.md)

## Description

mac-card: decode the parse goto payload, render the found, miss, and duplicate cards in place of the write preview, relabel the primary button, and dispatch the Go To on Return through the / landing path with an accept-time fresh parse.

## Notes

[2026-11-25T22:56:24Z · bob-cli-q7.4] PROPOSED FOLLOW-UP: Bring the existing docs pages under their word caps — `just docs-check` fails identically on clean base for plugin APIs, capture syntax, JSON outputs, Bob ledger tools, and Bob navigation hotkeys.

[2026-11-26T00:47:00Z · bob-cli-q7.4--3] Verified the similar-task draft-preservation change on committed tree 1e85be2600e29b48a3feb98bc34e1e9b0b00c0f8 (the green CI snapshot tree; snapshot 8900dd118988f969e2133ccdd55f8597cb2e1057). Mac bundle and test typecheck passed, portable-check passed (2,754 tests, 1 skipped), and exact-SHA macOS CI run 45727420737 passed all required checks. Current clean HEAD 4eb9b2e977dc8275a5849d5ac7f8bc8fabb617b2 descends from the tested commit; its only additional change is the drawer-fixture generator. The existing docs-check baseline follow-up remains recorded in phase note #1.

## Dependencies

- **Depends on:** [bob-cli-q7.1](bob-cli-q7.1.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q7.5](bob-cli-q7.5.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q7.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q7.4.md) | [bob-cli-q7.4](bob-cli-q7.4.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@fc0d455`](https://github.com/bobs-org/bob-mac-capture/commit/fc0d45515c8d86a33ab8b4ca46452f837eb3c490) | feat(capture): add caret Go To destination dispatch | [bob-cli-q7.4](bob-cli-q7.4.md) | 2026-11-25 18:03:57 EST |
| bob-mac-capture | [`bob-mac-capture@5d04d28`](https://github.com/bobs-org/bob-mac-capture/commit/5d04d286ffd485f2256bf7fc6dcb411a5dc2765e) | fix(ci): allow full Swift test suite to finish | [bob-cli-q7.4](bob-cli-q7.4.md) | 2026-11-25 18:35:40 EST |
| bob-mac-capture | [`bob-mac-capture@1e85be2`](https://github.com/bobs-org/bob-mac-capture/commit/1e85be2600e29b48a3feb98bc34e1e9b0b00c0f8) | fix(capture): preserve draft when opening similar tasks | [bob-cli-q7.4](bob-cli-q7.4.md) | 2026-11-25 19:06:15 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q7.4--1][1] | Need current phase scope, decisions, notes, and status before fixing the CI failure | 1 |
| read-by | [agent:bob-cli-q7.4--2][1] | Confirm phase status and recorded follow-up note before continuing its red CI gate | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q7.4.md

<!-- sase:referenced-by:end -->
