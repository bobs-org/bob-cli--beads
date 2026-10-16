# Bead: bob-cli-8f.2 — RefsCore decoding, fetcher, card state machine, and copy

[Bead Pages](../README.md) / [bob-cli-8f](README.md) / bob-cli-8f.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.7y](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.7y.md) · **Assignee:** `bob-cli-8f.2` · **Size:** medium
**Created:** 2026-10-16 10:04:17 EDT
**Plan:** [202610/refs\_link\_to\_today.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/refs_link_to_today.md)

## Description

mac_core: in bob-mac-capture's portable RefsCore/CaptureCore targets, decode the `ref today` envelope (reusing CaptureCommandSuccess). Add BobRefsFetcher.linkToToday with preview and write lanes, plus the pure RefsTodayLinkCard state machine (ranking, selection-to-selector mapping, stale-preview drop, running/failed/refused phases) and its key map. Add RefsTodayLinkPresentation for every string, row meta, lane chip, preview line, toast, notification, and announcement. Add a fake-bob `ref today` arm with real-bob fixtures and tests.

## Dependencies

- **Depends on:** [bob-cli-8f.1](bob-cli-8f.1.md) ✓ · ⧖ 2026-10-16
- **Blocks:** [bob-cli-8f.3](bob-cli-8f.3.md) ◐ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-8f.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8f.2/README.md) | [bob-cli-8f.2](bob-cli-8f.2.md) | 0 |
