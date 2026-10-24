# Bead: bob-cli-bk.3 — Decode inbox routes and send route answers in CaptureCore

[Bead Pages](../README.md) / [bob-cli-bk](README.md) / bob-cli-bk.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.a9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.a9.md) · **Assignee:** `bob-cli-bk.3` · **Size:** medium
**Created:** 2026-10-24 14:00:27 EDT · **Closed:** 2026-10-24 17:14:45 EDT
**Plan:** [202610/capture\_inbox\_routing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_inbox_routing.md)

## Description

mac-route-client: CaptureCore decodes `inbox_route`, sends answers and the guard flag behind a per-identity capability, models the route choice state, and documents the protocol.

## Notes

[2026-10-24T21:14:34Z · bob-cli-bk.3] PROPOSED FOLLOW-UP: skipped decisions:capture-asks-where-inbox-tasks-go record per epic memory_decision_record=no; mac-route-card land agent should decide whether the decisions-web record (bob detects/lists/moves, Mac only asks) is still wanted

[2026-10-24T21:14:45Z · bob-cli-bk.3] CaptureCore decodes inbox_route on success/failure with refused detail and choice_required/refused/stale codes; BobProcessClient sends repeated --inbox-route answers and --require-inbox-route-choice behind per-identity capability memory with guard retry; new CaptureInboxRouteChoiceState covers answers/filter/highlight/back-forward/refusal-reseed plus preview/success presentation; 8 real-bob fixtures + fake-bob knobs; 32 new tests, full suite 1642 pass, lint + docs-check clean on athena (Linux portable-check; no BobMacCapture sources touched so mac typecheck not needed)

## Dependencies

- **Depends on:** [bob-cli-bk.2](bob-cli-bk.2.md) ✓ · ⧖ 2026-10-24
- **Blocks:** [bob-cli-bk.4](bob-cli-bk.4.md) ◐ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bk.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bk.3/README.md) | [bob-cli-bk.3](bob-cli-bk.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@2968311`](https://github.com/bobs-org/bob-mac-capture/commit/2968311e5fa7924ed99bf83e52df865ee6e114c1) | feat(mac-capture): decode inbox routes and send route answers in CaptureCore | [bob-cli-bk.3](bob-cli-bk.3.md) | 2026-10-24 17:16:02 EDT |
