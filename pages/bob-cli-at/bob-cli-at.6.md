# Bead: bob-cli-at.6 — Bob Mac Capture receipt observer, notifications, and settings

[Bead Pages](../README.md) / [bob-cli-at](README.md) / bob-cli-at.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.56.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.56.linker.w0.md) · **Assignee:** `bob-cli-at.6` · **Size:** medium
**Created:** 2026-10-23 11:44:16 EDT · **Closed:** 2026-10-23 15:55:22 EDT
**Plan:** [202610/highlights\_coordinated\_marker\_writes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_coordinated_marker_writes.md)

## Description

mac-app: in bob-mac-capture, observe `org.bobs.bob.ref.scan-finished` with `notify_register_dispatch` and read the receipt off the main thread. Dedupe by content hash. Only when needed, check open tabs with the existing read-only Highlights tab reader, and never prompt for Accessibility. When the panel is hidden, post a passive, silent, threaded `refs-scan` notification that selects the row. When the panel is visible, show a footer clause or the busy banner with Scan Again. Notify for busy holds once per PDF. Add the Settings › References toggle "Tell me when Bob updates an open PDF" (on by default). ⌘S passes `-a`, with a remembered retry for an older bob. Update the refs, settings, and protocol docs, compile on the Mac where reachable, and rely on macOS CI.

## Notes

[2026-10-23T19:55:22Z · bob-cli-at.6] Wired RefsScanReceiptObserver (Darwin org.bobs.bob.ref.scan-finished, off-main bounded receipt, content-hash dedupe, tab check only when needed and already trusted), Settings toggle default-on, ⌘S -a with remembered clap-exit-2 retry, footer clauses and busy Scan Again banner, passive silent threaded refs-scan notifications that select the catalog row. just portable-check: 1554 tests, 0 failures (scan argv -a, attended retry+remember, PDF surface hide/disable/busy-dedupe, Darwin name). just docs-check passed (refs, settings, protocol). ssh mac timed out — macOS BobMacCapture compile/typecheck-tests unverified; macOS CI is the backstop. No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-at.5](bob-cli-at.5.md) ✓ · ⧖ 2026-10-23
- **Blocks:** [bob-cli-at.7](bob-cli-at.7.md) ✓ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-at.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-at.6/README.md) | [bob-cli-at.6](bob-cli-at.6.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-at.6][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-at.6/README.md

<!-- sase:referenced-by:end -->
