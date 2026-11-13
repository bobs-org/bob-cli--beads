# Bead: bob-cli-kx.3.1.4 — Notify once when sync archives mail

[Bead Pages](../README.md) / [bob-cli-kx.3.1](bob-cli-kx.3.1.md) / bob-cli-kx.3.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kx.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.3.md) · **Assignee:** `bob-cli-kx.3.1.4` · **Size:** small
**Created:** 2026-11-13 08:02:47 EST · **Closed:** 2026-11-13 10:55:54 EST
**Plan:** [202611/gmail\_archive\_receipts.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_receipts.md)

## Description

desktop_receipts: reuse the vault-sync desktop notification transport for newly durable archive outcomes with an inert undo command and no repeated notifications from historical receipts.

## Notes

[2026-11-13T15:50:49Z · bob-cli-kx.3.1.4] PROPOSED FOLLOW-UP: just lint fails on the clean base with 5 clippy deny-errors in src/native/gmail/unarchive.rs (needless_borrow at lines 283, 313, 330 and useless_conversion at line 464) from phase bob-cli-kx.3.1.3; verified identical failure with my changes stashed. Needs a small cleanup commit to unblock just check.

[2026-11-13T15:55:35Z · bob-cli-kx.3.1.4] PROPOSED FOLLOW-UP: just docs-check fails on the clean base with 3 word-budget overruns (docs/reference/json-outputs.md, docs/reference/plugins/bob-ledger-tools.md, docs/reference/plugins/bob-navigation-hotkeys.md); verified identical failure with my changes stashed. Needs trimming or budget relief from the docs owner/land agent.

[2026-11-13T15:55:54Z · bob-cli-kx.3.1.4] desktop_receipts done: shared desktop_notify transport reused by vault-sync, gmail sync notifies once per live run with archived thread ids and an inert bob gmail unarchive command (quiet-safe, opt-out honored, silent on preview/skip/failure/repeat, recovery notifies once). Verified: 9 new lib unit tests, 4 new fake-gog integration tests, full gmail_archive_apply (44), gmail_sync (42), gmail_archive_preview (4), vault_sync lib (12) green; fmt clean; docs-gen regenerated. Pre-existing clean-base failures recorded as follow-ups: 5 clippy deny-errors in unarchive.rs and 3 docs word-budget overruns.

## Dependencies

- **Depends on:** [bob-cli-kx.3.1.3](bob-cli-kx.3.1.3.md) ✓ · ⧖ 2026-11-13
- **Blocks:** [bob-cli-kx.3.1.5](bob-cli-kx.3.1.5.md) ◐ · ⧖ 2026-11-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kx.3.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.3.1.4/README.md) | [bob-cli-kx.3.1.4](bob-cli-kx.3.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`cd6aefa`](https://github.com/bobs-org/bob-cli/commit/cd6aefae7974e11557d3d84268ac397b19e993a9) | feat(gmail)!: notify once when sync archives mail | [bob-cli-kx.3.1.4](bob-cli-kx.3.1.4.md) | 2026-11-13 10:57:56 EST |
