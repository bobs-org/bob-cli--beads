# Bead: bob-cli-kd.4.1.1 — Parse bank exports and establish the shared journal

[Bead Pages](../README.md) / [bob-cli-kd.4.1](bob-cli-kd.4.1.md) / bob-cli-kd.4.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kd.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kd.4.md) · **Assignee:** `bob-cli-kd.4.1.1` · **Size:** medium
**Created:** 2026-11-11 14:24:04 EST · **Closed:** 2026-11-11 15:04:45 EST
**Plan:** [202611/bank\_import.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_import.md)

## Description

sources-journal: parse both OFX dialects and the Wells Fargo CSV profile, resolve account aliases, hash identities, and expose a validated per-host bank journal with bounded diagnostics and balance-phase input types.

## Notes

[2026-11-11T20:04:31Z · bob-cli-kd.4.1.1] PROPOSED FOLLOW-UP: just lint fails on HEAD at src/native/vault_git.rs:65 items_after_test_module (is_ignored after the cfg(test) module) from 1a9b6828 — reproduces on the clean base tree, out of this phase scope.

[2026-11-11T20:04:45Z · bob-cli-kd.4.1.1] Verified cargo test --lib native::bank:: (51 passed): SGML/XML equivalence, CHARSET/BOM/CRLF, CSV quoting and occurrence ids, invalid money/date/truncated input, empty OFX coverage/balance, inferred/explicit/ambiguous/cash account resolution, exact sha256(alias\\n bank_id), 8-to-12 prefix collision and refused 12-char collision, masked desc with no raw FITID/account numbers in serialized events, multi-host fold with money contradictions, and bounded bank_journal_malformed on bob bank check.

Published APIs for bob-cli-kd.5 and later import phases:
- bank::source::{parse_export, resolve_account, ParsedStatement, ParsedTransaction, ResolvedStatement, SourceKind, SourceError}
- bank::identity::{transaction_key, sha256_hex, mask_digits, merchant_key, IdReservation}
- bank::journal::{load, serialize_import, serialize_txn, JournalSnapshot, ImportEvent, TxnEvent, TxnOutcome, ImportCounts, NewImport, NewTxn, NAMESPACE=.bob/bank}
- pref_journal::parse_envelope
- check finding bank_journal_malformed (warning, pref_journal bound of 8 plus summary)

Raw FITID and account numbers stay in transient parse state only. No --epic-symbol leftovers.

## Dependencies

- **Blocks:** [bob-cli-kd.4.1.2](bob-cli-kd.4.1.2.md) ◐ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kd.4.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.4.1.1/README.md) | [bob-cli-kd.4.1.1](bob-cli-kd.4.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bffbf36`](https://github.com/bobs-org/bob-cli/commit/bffbf36bd58d79868e4bf2b2db042bcab50f4635) | feat(bank): parse OFX/CSV exports and fold the bank journal | [bob-cli-kd.4.1.1](bob-cli-kd.4.1.1.md) | 2026-11-11 15:06:39 EST |
