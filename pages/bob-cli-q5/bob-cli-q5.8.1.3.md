# Bead: bob-cli-q5.8.1.3 — Observe receipts and hold notices until return

[Bead Pages](../README.md) / [bob-cli-q5.8.1](bob-cli-q5.8.1.md) / bob-cli-q5.8.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.md) · **Assignee:** `bob-cli-q5.8.1.3` · **Size:** medium
**Created:** 2026-11-26 12:54:20 EST · **Closed:** 2026-11-26 16:01:37 EST
**Plan:** [202611/mac\_snooze\_wake\_notice.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_snooze_wake_notice.md)

## Description

notice-runtime: implement the Darwin observer, atomic notifier claim, persistent wake-id deduplication, macOS presence adapter, settings storage, and app-lifetime delivery coordinator behind injected presentation callbacks. Claim only when a compatible client and live presenter are attached.

## Notes

[2026-11-26T21:01:37Z · bob-cli-q5.8.1.3--2] Mac scratch green: just typecheck-tests 4 PASS (BobMacCaptureTests, InstallHelper, CaptureCore, RefsCore) + bundle.sh ad-hoc sign success (exit 0, /tmp/mac-verify-fix2). just portable-check green: 2908 tests, 0 failures, 1 skipped. Fixes: AppKit import for NSWorkspace tests, de-async harness helpers, async readReceipt for coalesce.

## Dependencies

- **Depends on:** [bob-cli-q5.8.1.2](bob-cli-q5.8.1.2.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-q5.8.1.4](bob-cli-q5.8.1.4.md) ✓ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.8.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.3.md) | [bob-cli-q5.8.1.3](bob-cli-q5.8.1.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.8.1.3--2][1] | close bead after green mac verification | 2 |
| read-by | [agent:bob-cli-q5.8.1.5][2] | Need sibling phase status to avoid duplication | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.3.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.8.1.5/README.md

<!-- sase:referenced-by:end -->
