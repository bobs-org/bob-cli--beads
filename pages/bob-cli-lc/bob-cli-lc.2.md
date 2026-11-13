# Bead: bob-cli-lc.2 — Clean Wells Fargo QFX payees and merchant keys

[Bead Pages](../README.md) / [bob-cli-lc](README.md) / bob-cli-lc.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1c7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1c7.md) · **Assignee:** `bob-cli-lc.2` · **Size:** medium
**Created:** 2026-11-13 10:55:28 EST · **Closed:** 2026-11-13 12:06:01 EST
**Plan:** [202611/bank\_weekly\_category\_walk.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_weekly_category_walk.md)

## Description

qfx-cleaning: teach naming.rs the real QFX description shapes so payees lose dates, places, card digits, order codes, and the account holder's name; merchant keys collapse repeat merchants; learned payees are re-cleaned; the default account stops getting [acct::].

## Notes

[2026-11-13T16:41:22Z · bob-cli-lc.2] PROPOSED FOLLOW-UP: Bring the unchanged mounted plugin reference pages under the 6,000-word docs-check cap: bob-ledger-tools.md (6,136 words) and bob-navigation-hotkeys.md (6,055 words) fail on clean base; prior navigation tracking was bob-cli-jz, now closed.

[2026-11-13T17:05:21Z · bob-cli-lc.2--2] PROPOSED FOLLOW-UP: Fix the five baseline Clippy errors in src/native/gmail/unarchive.rs: needless_borrow at line 283 (two occurrences), 313, and 330; explicit_into_iter_loop at line 464. just lint reproduced them on detached clean HEAD in monitor wehg68kx6ce9, confirming they are unrelated to this bank phase.

[2026-11-13T17:06:01Z · bob-cli-lc.2--2] Completed the bank QFX payee-cleaning phase. just check failed on five Clippy errors in unchanged src/native/gmail/unarchive.rs; just lint reproduced the same errors on detached clean HEAD (monitor wehg68kx6ce9), so the failure is unrelated to this phase. Recorded the Gmail lint repair as a proposed follow-up. The phase epic-symbol check reports no remaining entries.

## Dependencies

- **Blocks:** [bob-cli-lc.3](bob-cli-lc.3.md) ✓ · ⧖ 2026-11-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-lc.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-lc.2.md) | [bob-cli-lc.2](bob-cli-lc.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d6d755a`](https://github.com/bobs-org/bob-cli/commit/d6d755a1da262080f5a78196a653f5f296017475) | feat(bank): clean QFX payees and merchant keys | [bob-cli-lc.2](bob-cli-lc.2.md) | 2026-11-13 12:08:10 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-lc.2--2][1] | Confirm the phase is closed with the clean-HEAD lint blocker and follow-up recorded | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-lc.2.md

<!-- sase:referenced-by:end -->
