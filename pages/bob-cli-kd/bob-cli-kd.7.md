# Bead: bob-cli-kd.7 — End-to-end proof, the guide, docs audit, memory, and follow-ups

[Bead Pages](../README.md) / [bob-cli-kd](README.md) / bob-cli-kd.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1be](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1be.md) · **Assignee:** `bob-cli-kd.7` · **Size:** medium
**Created:** 2026-11-11 11:24:16 EST · **Closed:** 2026-11-12 09:38:23 EST
**Plan:** [202611/bank\_daily\_acknowledgment.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_daily_acknowledgment.md)

## Description

bank-wrapup: walk every bank gesture end to end in a temporary vault, write the how-to guide, audit every bank doc against shipped behaviour, check the real vault, apply only the accepted memory decisions, and propose the subscriptions album (blocked on bob-cli-k3) and the later views as follow-ups.

## Notes

[2026-11-12T14:37:44Z · bob-cli-kd.7] PROPOSED FOLLOW-UP: subscriptions album — design the discretionary subscriptions album (subscriptions_scope=discretionary from this epic); it must depend on bob-cli-k3 (`sase bead dep add <new-task> bob-cli-k3`). Recurring charges stay out of bank month notes.

[2026-11-12T14:37:50Z · bob-cli-kd.7] PROPOSED FOLLOW-UP: later bank views after a 2–4 week trial with at least two months of rows — typical week/month comparisons in the month card, a year card, a bank Stats metric, a bank line in Bob Mac Capture idle agenda (bob JSON first, thin client), and a week-note fence.

[2026-11-12T14:37:56Z · bob-cli-kd.7] PROPOSED FOLLOW-UP: read-only feed spike (SimpleFIN or Teller) only if the trial shows the weekly Wells Fargo QFX download is the friction.

[2026-11-12T14:38:02Z · bob-cli-kd.7] PROPOSED FOLLOW-UP: docs-check strict Zensical fails on mounted bob-plugins `docs/develop/validation.md` link `../bob-vim-yank-flash.md#verification` (page lives at `docs/reference/plugins/bob-vim-yank-flash.md`). Lint and generated-drift passed. Reproduces from the plugin mount; this phase did not edit that page. HEAD mkdocs already includes Plugin development.

[2026-11-12T14:38:23Z · bob-cli-kd.7] Verified bank-wrapup end to end.

E2E (tests/cli/bank.rs, six tests, all pass):
- walk_ensure_type_list_report_ack_and_import_twice: ensure today; type Smashburger/7-Eleven/cash-cart/ShopRite-waiting/payroll/empty stub; check flagged; list 1 waiting; report month/W46/day; ack day; import 1 new/3 matched then replay 0 new/4 seen; checking balanced
- typed_twin_amount_mismatch_and_ambiguous_tie: $20 vs $24 Tab twins + equidistant $5 Coffee
- deleted_row_shows_delta_then_force_restores: missing row → delta → import -F restored==1
- skipped_week_is_a_named_gap: gap + bank_coverage_gap
- card_payment_nets_out_and_a_credit_is_never_income: out/in/refund/transfer/unclassified
- malformed_file_refuses_the_batch: exit 2, month/journal/HEAD unchanged

Live temp-vault transcript (BOB_NOW=2026-11-12T12:00:00):
$ bob bank ensure → Created bank/2026-11.md / bank/2026-11.md:16
$ bob bank check → ✓ 2 notes — 0 errors, 0 warnings
$ bob bank → nothing to acknowledge; WF Checking unverified; Pocket cash untracked
$ bob bank report → November 2026 so far; Out $0.00
(typed Smashburger [x] + ShopRite [ ])
$ bob bank → 1 to acknowledge ShopRite
$ bob bank ack -D today → ✓ Acknowledged 1 row ShopRite
$ bob bank → nothing to acknowledge

Guide: docs/guides/acknowledge-bank-transactions.md under Plan the day; contracts.yml reader; pointers from bank.md and vault-format.md.
Memory: glossary:bank-month-note and glossary:bank-row only (memory_bank_decision=no).
Docs: just docs-gen ok; docs-check lint+drift pass; strict Zensical fails on mounted bob-plugins validation.md (PROPOSED FOLLOW-UP).
Real vault (checking only): check 0 findings; list 0 waiting; report Nov 2026 so far, checking unverified, 0 rows in bank/2026-11.md. No checking_card.
Report, did not close: bob.md ^bank-records still [/] “Use records to start tracking bank transactions again!”. cash.md ^balance is the snapshot heading; the 30-day recur.md chore is [?] scheduled 2026-12-01 and becomes optional once checking shows ✓ balanced.
epic-symbols: none leftover. Did not close parent epic bob-cli-kd.

## Dependencies

- **Depends on:** [bob-cli-kd.1](bob-cli-kd.1.md) ✓ · ⧖ 2026-11-11
- **Depends on:** [bob-cli-kd.5](bob-cli-kd.5.md) ✓ · ⧖ 2026-11-11
- **Depends on:** [bob-cli-kd.6](bob-cli-kd.6.md) ✓ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kd.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.7/README.md) | [bob-cli-kd.7](bob-cli-kd.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`65c9e95`](https://github.com/bobs-org/bob-cli/commit/65c9e95c71309f0d124e7fee8309a4daa976f701) | docs(bank): add the acknowledgment guide and end-to-end CLI proof | [bob-cli-kd.7](bob-cli-kd.7.md) | 2026-11-12 09:40:12 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:research.49.cdx][1] | Establish initial vault rollout and end-to-end verification state | 1 |
| read-by | [agent:research.49.cld][2] | research: user guide for first-time bank ack and e2e test of bob-cli-kd | 1 |
| read-by | [agent:research.49.final][3] | Check sub-phase state and any notes for the consolidated kd e2e test gating | 1 |
| read-by | [agent:research.49.gem][4] | Understand phase 7 scope and e2e testing requirements | 1 |
| read-by | [agent:research.49.grk][5] | Need closed restart/CLI phases and wrap-up e2e proof so the first-run guide matches shipped work | 1 |
| read-by | [agent:research.49.mus][6] | research kd epic phase scope for user guide | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.cdx/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.cld/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.final/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.gem/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.grk/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.mus/README.md

<!-- sase:referenced-by:end -->
