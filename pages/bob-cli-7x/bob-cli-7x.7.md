# Bead: bob-cli-7x.7 — RefsCore rename contract, fetcher, stores, and card state

[Bead Pages](../README.md) / [bob-cli-7x](README.md) / bob-cli-7x.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.1k.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.1k.linker.w0.md) · **Assignee:** `bob-cli-7x.7` · **Size:** medium
**Created:** 2026-10-15 15:25:59 EDT · **Closed:** 2026-10-15 17:33:44 EDT
**Plan:** [202610/bob\_ref\_rename.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_ref_rename.md)

## Description

mac-rename-core: in bob-mac-capture RefsCore, decode the ref rename report, add RefsFetching.rename on a non-cancelling refs-rename lane, map older-bob and error envelopes, add RefsOpenLogStore.rename(from:to:), pure rename-card state, key map, and presentation strings; fake-bob branch and portable tests.

## Notes

[2026-10-15T21:33:44Z · bob-cli-7x.7--5] Implemented reference rename decoding, non-cancelling fetch lane, error mapping, open-log path updates, and rename card state/presentation with fixtures and portable tests; removed temporary fixture instrumentation. Bob Mac Capture just portable-check passed on athena, and epic-symbol check reported none.

## Dependencies

- **Depends on:** [bob-cli-7x.3](bob-cli-7x.3.md) ✓ · ⧖ 2026-10-15
- **Blocks:** [bob-cli-7x.8](bob-cli-7x.8.md) ◐ · ⧖ 2026-10-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7x.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7x.7.md) | [bob-cli-7x.7](bob-cli-7x.7.md) | 0 |
