# Bead: bob-cli-an.6.6.6.5.6.5.4 — Restore Mac save-key test compilation and the mounted Refs docs gate

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5](bob-cli-an.6.6.6.5.6.5.md) / bob-cli-an.6.6.6.5.6.5.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.land--2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.4` · **Size:** medium
**Created:** 2026-10-24 12:31:54 EDT · **Closed:** 2026-10-24 12:48:23 EDT
**Plan:** [202610/backlog\_batch7\_url\_identity\_gist\_metadata\_close\_summary\_mac\_ci.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch7_url_identity_gist_metadata_close_summary_mac_ci.md)

## Description

mac-save-ci: resolve bob-cli-bg and bob-cli-bh in bob-mac-capture, preserving event conversion and documentation contracts, with compiled Mac tests and the shared docs gate.

## Notes

[2026-10-24T16:48:23Z · bob-cli-an.6.6.6.5.6.5.4] bg: moved NSEvent init into extension in HighlightsSaveKeyMonitor.swift, restoring memberwise init used by HighlightsSaveKeyMonitorTests commandS helper; portable-check green (1587 tests, 0 failures, swift-format clean); exact struct+call shape typechecks with swiftc; macOS XCTest compile not verified locally because mac is offline (ssh+tailscale ping timeout), CI executes tests. bh: condensed source docs/refs.md 6027->5897 lint words, mounted page 5871 words vs 6000 cap; save-scan behavior/permissions/defaults/keyboard contracts retained; just docs-check green with BOB_DOCS_BOB_MAC_CAPTURE_DIR mounted (lint ok, 447 passed). Target tasks bob-cli-bg/bh left open for lander; no epic-symbols.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.4/README.md) | [bob-cli-an.6.6.6.5.6.5.4](bob-cli-an.6.6.6.5.6.5.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.4][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.4/README.md

<!-- sase:referenced-by:end -->
