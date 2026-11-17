# Bead: bob-cli-ms.4 — Record update service and guarded session with direct apply

[Bead Pages](../README.md) / [bob-cli-ms](README.md) / bob-cli-ms.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.55.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.55.linker.w0.md) · **Assignee:** `bob-cli-ms.4` · **Size:** medium
**Created:** 2026-11-17 11:29:54 EST · **Closed:** 2026-11-17 16:22:18 EST
**Plan:** [202611/record\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_card.md)

## Description

record-session: plugin service for records show/update, a record session over the shared guarded session with an opt-in direct-apply path, inverse-op Undo, pane saves, auto-sync echo suppression, an optimistic sheet overlay, and a real-bob writer matrix.

## Notes

[2026-11-17T21:21:37Z · bob-cli-ms.4] PROPOSED FOLLOW-UP: just docs-check / plugins docs:check fail on docs/reference/json-outputs.md 6089/6000 words — identical on clean bob-cli; already cited by closed bob-cli-ms.2 and open epic bob-cli-mr.3.1

[2026-11-17T21:21:44Z · bob-cli-ms.4] PROPOSED FOLLOW-UP: full bob-plugins npm test 25ms wall-clock flakes under suite load — event-link-times 139.9ms (bob-cli-km READY), frees-marks 41ms (bob-cli-io READY), keep-moving-marks-surface 2007ms (bob-cli-ki READY), off-clock-link-chips 203.5ms (bob-cli-ju READY); isolated record-update tests pass

[2026-11-17T21:21:51Z · bob-cli-ms.4] PROPOSED FOLLOW-UP: obsidian-album-schema-writer-e2e --self-test held-lock apply must create exactly one commit, saw 2 — reproduces identically on clean plugins tree at 137c77f with this phase stashed; no existing bead found

[2026-11-17T21:21:58Z · bob-cli-ms.4] PROPOSED FOLLOW-UP: bob plugins sync refused vault bob-ledger-tools 1.129.0 from abandoned dirty bob-cli_15 (source_head b0a9c89, 2026-11-17T18:48:30Z, digest cd40fa09…, host apollo); no ws15 agent, HEAD..@{upstream} empty, no reachable commit holds vault bytes; did not pass -F — force would drop that dirty 1.129.0 record-sheet-era deploy

[2026-11-17T21:22:18Z · bob-cli-ms.4] Shipped bob-ledger-tools 1.130.0 record write machine: records show/update JSON wrappers, opt-in applyOps on the shared guarded session, inverse-op Undo, pane saves [recordPath,albumPath], own-path echo suppression plus albumInvalidate(record-update), 5s overlay TTL, capability record_values_v1. 14 unit tests plus real-bob writer e2e (CRLF preserved, BOM record_uneditable keeps bytes). Album/bank still refuse applyOps. plugins sync refused abandoned ws15 1.129.0 dirty vault; no -F. Known suite reds recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-ms.2](bob-cli-ms.2.md) ✓ · ⧖ 2026-11-17
- **Depends on:** [bob-cli-ms.3](bob-cli-ms.3.md) ✓ · ⧖ 2026-11-17
- **Blocks:** [bob-cli-ms.5](bob-cli-ms.5.md) ◐ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ms.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ms.4/README.md) | [bob-cli-ms.4](bob-cli-ms.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@f49e175`](https://github.com/bobs-org/bob-plugins/commit/f49e175436ce002e48e258bc60bc433b3167190e) | feat(ledger-tools): add record update session and writer | [bob-cli-ms.4](bob-cli-ms.4.md) | 2026-11-17 16:24:19 EST |
