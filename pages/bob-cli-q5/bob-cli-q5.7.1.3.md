# Bead: bob-cli-q5.7.1.3 — Wake snoozed tasks while the capture panel is hidden

[Bead Pages](../README.md) / [bob-cli-q5.7.1](bob-cli-q5.7.1.md) / bob-cli-q5.7.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.7.md) · **Assignee:** `bob-cli-q5.7.1.3` · **Size:** medium
**Created:** 2026-11-26 07:49:18 EST · **Closed:** 2026-11-26 10:44:44 EST
**Plan:** [202611/mac\_snoozed\_agenda.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_snoozed_agenda.md)

## Description

snooze-waker: add the schema-checked non-cancelling Bob wake lane and app-owned SnoozeWakeScheduler, with bounded retries and lifecycle invalidation. Include snooze instants in visible boundary refresh, verify integration with fake time and fake Bob, and document the command and lane contracts.

## Notes

[2026-11-26T15:44:44Z · bob-cli-q5.7.1.3--1] Verified: docs-check passed; portable-check passed all 2,837 Swift tests (one skipped); Mac scratch bundle and just typecheck-tests succeeded; exact-SHA macos-ci-check passed run 45847440694 at f923059807e9efa942476d1a51bb7388d26c9efe with build, tests, bundle/signature, launch smoke, and install/reinstall checks. epic-symbols had no leftovers.

## Dependencies

- **Depends on:** [bob-cli-q5.7.1.2](bob-cli-q5.7.1.2.md) ✓ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.7.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.7.1.3.md) | [bob-cli-q5.7.1.3](bob-cli-q5.7.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@a4a7020`](https://github.com/bobs-org/bob-mac-capture/commit/a4a7020d9e22ed992ce04a9d198b14dcf87ba65e) | feat(capture): wake snoozed tasks while panel is hidden | [bob-cli-q5.7.1.3](bob-cli-q5.7.1.3.md) | 2026-11-26 10:46:12 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.7.1.3--1][1] | Review final monitored verification before closing the phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.7.1.3.md

<!-- sase:referenced-by:end -->
