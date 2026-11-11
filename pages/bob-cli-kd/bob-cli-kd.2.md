# Bead: bob-cli-kd.2 — The bank module, row grammar, and bob bank check

[Bead Pages](../README.md) / [bob-cli-kd](README.md) / bob-cli-kd.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1be](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1be.md) · **Assignee:** `bob-cli-kd.2` · **Size:** medium
**Created:** 2026-11-11 11:24:16 EST · **Closed:** 2026-11-11 12:15:27 EST
**Plan:** [202611/bank\_daily\_acknowledgment.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_daily_acknowledgment.md)

## Description

bank-grammar: add `src/native/bank/` with the `bank:` config parser (key-path diagnostics), the row and day-heading grammar, the canonical renderers and insertion planners, and the month-note scanner. Ship the read-only `bob bank check` lint in the Integrations section, and write `docs/bank.md` as the contract.

## Notes

[2026-11-11T17:15:13Z · bob-cli-kd.2] PROPOSED FOLLOW-UP: docs-check fails on mounted sibling reference pages over the 6000-word cap (mac-capture capture-panel/previews/keyboard/protocol; plugins bob-ledger-tools/bob-navigation-hotkeys). They are gitignored mounts and fail identically without this phase files. json-outputs.md stayed under the cap after the bank pointer.

[2026-11-11T17:15:27Z · bob-cli-kd.2] Shipped src/native/bank/ (config, grammar, month, scan, check, CLI) and bob bank check in Integrations. Verified: 22 bank unit tests; NativeCommand wiring tests; just lint; just docs-gen; live vault bob bank check -f json ok with schema_version 1, 2 notes, 0 errors, 0 warnings, 1 checking account, 18 categories; teaching empty, findings table, #task invisibility. docs/bank.md is the contract. Memory unedited (wrap-up only). No leftover --epic-symbol entries.

[2026-11-11T17:33:14Z · bob-cli-kd.2--1] just check failed on catalog count 91 vs 92 and root help snapshots missing bank. Bumped ENTRIES/catalog tests to 92, asserted bank-check, and added bank under Integrations in help fixtures. Re-verified document_shape, protocol_1, and root_help snapshots.

## Dependencies

- **Blocks:** [bob-cli-kd.3](bob-cli-kd.3.md) ◐ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kd.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kd.2.md) | [bob-cli-kd.2](bob-cli-kd.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`07f1c74`](https://github.com/bobs-org/bob-cli/commit/07f1c7442bb24d50658167856fb5816312199423) | feat(bank): add bank grammar, month notes, and read-only bob bank check | [bob-cli-kd.2](bob-cli-kd.2.md) | 2026-11-11 12:58:45 EST |
