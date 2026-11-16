# Bead: bob-cli-ls.6 — The bob bank subscriptions command

[Bead Pages](../README.md) / [bob-cli-ls](README.md) / bob-cli-ls.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1cp](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1cp.md) · **Assignee:** `bob-cli-ls.6` · **Size:** medium
**Created:** 2026-11-15 13:11:22 EST · **Closed:** 2026-11-15 19:49:34 EST
**Plan:** [202611/bank\_subscriptions\_album.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_subscriptions_album.md)

## Description

report: add the read-only bob bank subscriptions report with beautiful human output and the JSON contract every plugin surface reads, plus the audit guide.

## Notes

[2026-11-16T00:49:20Z · bob-cli-ls.6] PROPOSED FOLLOW-UP: docs-check reference budget fails on untouched docs/reference/plugins/bob-ledger-tools.md (6146 words vs 6000 cap on the clean base tree); trim in its owning phase

[2026-11-16T00:49:34Z · bob-cli-ls.6] bob bank subscriptions ships: clap wiring (-a/-b/-f), status-ordered human report with estimates and flags, JSON ledger contract (album/totals/subscriptions/findings/issues), audit-subscriptions guide + docs. Verified: just check exit 0 (fmt, clippy, 7 new unit tests, new bank e2e, catalog/help snapshot updates), just docs-gen exit 0, temp-vault smoke of human/JSON/hide-cancelled/price-flag/invalid-album. Also repaired stale 4-arg compute_ledger call left by closed ls.5 so the tree compiles. docs-check still fails only on pre-existing bob-ledger-tools.md budget overrun (file untouched; recorded as follow-up).

## Dependencies

- **Depends on:** [bob-cli-ls.2](bob-cli-ls.2.md) ✓ · ⧖ 2026-11-15
- **Depends on:** [bob-cli-ls.5](bob-cli-ls.5.md) ✓ · ⧖ 2026-11-15
- **Blocks:** [bob-cli-ls.8](bob-cli-ls.8.md) ◐ · ⧖ 2026-11-15
- **Blocks:** [bob-cli-ls.9](bob-cli-ls.9.md) ◐ · ⧖ 2026-11-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ls.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.6/README.md) | [bob-cli-ls.6](bob-cli-ls.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f252f18`](https://github.com/bobs-org/bob-cli/commit/f252f1856abc3ef2f12c6e7555f7c6964b484979) | feat(bank): add bank subscriptions report command | [bob-cli-ls.6](bob-cli-ls.6.md) | 2026-11-15 19:52:02 EST |
