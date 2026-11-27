# Bead: bob-cli-q5.8.1.6.1 — Restore the build and verify each wake against a fresh bob read

[Bead Pages](../README.md) / [bob-cli-q5.8.1.6](bob-cli-q5.8.1.6.md) / bob-cli-q5.8.1.6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.8.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.land.md) · **Assignee:** `bob-cli-q5.8.1.6.1` · **Size:** medium
**Created:** 2026-11-26 20:05:50 EST · **Closed:** 2026-11-26 22:43:30 EST
**Plan:** [202611/mac\_snooze\_wake\_notice\_repair.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_snooze_wake_notice_repair.md)

## Description

runtime-verify: fix the StatusItemGlyph build break, make every accepted receipt verify against a bob snooze read started after it, deliver immediately when nothing held, gate and atomically publish the notifier claim, and make the snooze process lanes serialize writes, surface bob refusals, and never cancel each other.

## Notes

[2026-11-27T03:43:30Z · bob-cli-q5.8.1.6.1--6] Verified exact-SHA macOS CI passed on snapshot 9af75ccb0db12ced484982df0b2dd3fdb71b43e5 (run 45932873351), including Test, Bundle, signature verification, launch smoke test, and install/reinstall; epic-symbols reported no entries for this phase.

## Dependencies

- **Blocks:** [bob-cli-q5.8.1.6.2](bob-cli-q5.8.1.6.2.md) ✓ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.8.1.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.6.1.md) | [bob-cli-q5.8.1.6.1](bob-cli-q5.8.1.6.1.md) | 4 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@d2294ec`](https://github.com/bobs-org/bob-mac-capture/commit/d2294eca0e2e64c01e86cc44039b6ae3903e6540) | fix(snooze): verify wake notices against fresh state | [bob-cli-q5.8.1.6.1](bob-cli-q5.8.1.6.1.md) | 2026-11-26 20:48:23 EST |
| bob-mac-capture | [`bob-mac-capture@d479a51`](https://github.com/bobs-org/bob-mac-capture/commit/d479a515838ffefe5cda1f213e83ac08752f9ae8) | test(snooze): make XCTest captures explicit | [bob-cli-q5.8.1.6.1](bob-cli-q5.8.1.6.1.md) | 2026-11-26 21:16:24 EST |
| bob-mac-capture | [`bob-mac-capture@6aeab03`](https://github.com/bobs-org/bob-mac-capture/commit/6aeab03a3b44386aeb1c4c3f68c12521259b5a90) | fix(snooze): repair wake notification retries and routing | [bob-cli-q5.8.1.6.1](bob-cli-q5.8.1.6.1.md) | 2026-11-26 21:42:18 EST |
| bob-mac-capture | [`bob-mac-capture@ff55adb`](https://github.com/bobs-org/bob-mac-capture/commit/ff55adbc70bd47c1a7173ad2b6f5467df5faa870) | test(snooze): align day-purge handled-id expectation | [bob-cli-q5.8.1.6.1](bob-cli-q5.8.1.6.1.md) | 2026-11-26 22:12:02 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.8.1.6.1--2][1] | Need phase scope and notes before finishing the assigned snooze wake repair | 1 |
| read-by | [agent:bob-cli-q5.8.1.6.1--3][1] | Review phase state before fixing its failed exact-SHA gate | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.6.1.md

<!-- sase:referenced-by:end -->
