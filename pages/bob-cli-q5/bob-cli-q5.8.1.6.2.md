# Bead: bob-cli-q5.8.1.6.2 — Take day, vault, presence, and meeting facts from their real owners

[Bead Pages](../README.md) / [bob-cli-q5.8.1.6](bob-cli-q5.8.1.6.md) / bob-cli-q5.8.1.6.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.8.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.land.md) · **Assignee:** `bob-cli-q5.8.1.6.2` · **Size:** medium
**Created:** 2026-11-26 20:05:50 EST · **Closed:** 2026-11-26 23:03:12 EST
**Plan:** [202611/mac\_snooze\_wake\_notice\_repair.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_snooze_wake_notice_repair.md)

## Description

runtime-facts: use bob's date/now and vault_root as the authorities, hold instead of delivering when the agenda has no same-day facts, sample presence at launch, and re-evaluate when a meeting starts while a notice is on screen.

## Notes

[2026-11-27T04:03:12Z · bob-cli-q5.8.1.6.2] runtime-facts done in bob-mac-capture working tree (uncommitted, for land agent to push): bob day/vault from list read, day/vault/duplicate deferred until fresh verification, symlink-safe Settings vault compare, agenda-unavailable hold with bounded refresh, stale same-day events still hold, overlapping meetings hold past first end, launch lock/session/display sampling, mid-display meeting-start re-evaluation. Verified: swift build --build-tests ok; SnoozeWakeNoticePolicyTests 37/37 pass; full portable suite 2923 tests with 1 flaky MeetingNotesSessionTests failure that passes in isolation on both trees. Mac compile/typecheck/CI not run here (AppKit needs macOS/CI); land agent to run macos-ci-check and watch exact-SHA run green.

## Dependencies

- **Depends on:** [bob-cli-q5.8.1.6.1](bob-cli-q5.8.1.6.1.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-q5.8.1.6.3](bob-cli-q5.8.1.6.3.md) ✓ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.8.1.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.8.1.6.2/README.md) | [bob-cli-q5.8.1.6.2](bob-cli-q5.8.1.6.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@9f9157f`](https://github.com/bobs-org/bob-mac-capture/commit/9f9157f7dc527ff7dc8a9f7bfaf07308d69b4d72) | fix(snooze): take day, vault, presence, and meeting facts from their real owners | [bob-cli-q5.8.1.6.2](bob-cli-q5.8.1.6.2.md) | 2026-11-26 23:04:06 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.8.1.6.2][1] | check notes and remaining work | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.8.1.6.2/README.md

<!-- sase:referenced-by:end -->
