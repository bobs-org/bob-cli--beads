# Bead: bob-cli-ls.5 — Subscription findings in bob bank check

[Bead Pages](../README.md) / [bob-cli-ls](README.md) / bob-cli-ls.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1cp](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1cp.md) · **Assignee:** `bob-cli-ls.5` · **Size:** medium
**Created:** 2026-11-15 13:11:22 EST · **Closed:** 2026-11-15 18:45:18 EST
**Plan:** [202611/bank\_subscriptions\_album.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_subscriptions_album.md)

## Description

check: report charged-after-cancel, still-charging, price-change, candidate, invalid-needle, overlap, and unknown-category findings, with paste-ready fixes. A bank rule doubles as a candidate's dismissal.

## Notes

[2026-11-15T23:29:12Z · bob-cli-ls.5] PROPOSED FOLLOW-UP: Restore docs/reference/plugins/bob-ledger-tools.md below the 6,000-word cap (already tracked by bob-cli-il) — just docs-check reports 6,055 words on this phase and reproduces the identical failure on clean HEAD 055f9b6e, so no duplicate task is needed.

[2026-11-15T23:45:18Z · bob-cli-ls.5--1] Verified the final phase diff with git diff --check and ran the requested gates: just all passed; just docs-check remains blocked only by the clean-base bob-ledger-tools 6,000-word cap issue already tracked by bob-cli-il. epic-symbols reported no leftovers.

## Dependencies

- **Depends on:** [bob-cli-ls.2](bob-cli-ls.2.md) ✓ · ⧖ 2026-11-15
- **Blocks:** [bob-cli-ls.6](bob-cli-ls.6.md) ◐ · ⧖ 2026-11-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ls.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ls.5.md) | [bob-cli-ls.5](bob-cli-ls.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`cfd4548`](https://github.com/bobs-org/bob-cli/commit/cfd4548a2cd60a165fdbdc67bd0472e2d6968343) | feat(bank): add native bank checks and subscription registry | [bob-cli-ls.5](bob-cli-ls.5.md) | 2026-11-15 18:48:43 EST |
