# Bead: bob-cli-ls.2.1 — Subscription registry, attribution, and ledger core

[Bead Pages](../README.md) / [bob-cli-ls.2](bob-cli-ls.2.md) / bob-cli-ls.2.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ls.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ls.2.md) · **Assignee:** `bob-cli-ls.2.1.land`
**Created:** 2026-11-15 13:23:48 EST · **Closed:** 2026-11-15 17:54:09 EST
**Plan:** [202611/subscription\_core.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/subscription_core.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/subscription_core.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/subscription_core.md

<!-- sase:links:end -->

## Description

Complete bob-cli-ls.2 with one reusable subscription resolver and ledger, guarded registry inputs, and additive bank row JSON.

## Notes

[2026-11-15T21:00:06Z · bob-cli-lr.land] DISCOVERED ISSUE (found by the bob-cli-lr land agent, 2026-11-15): on origin/master d794e0ba, just check fails in the clippy step (-D unused) on the subscription registry from c59b5b80 (bob-cli-ls.2.1.1), which nothing calls yet. Errors: unused import RecordField (src/native/bank/subscriptions/registry.rs:19); unused re-exports resolve_match/SubscriptionMatch and parse_subscription_snapshot/Subscription* (src/native/bank/subscriptions/mod.rs:6-11); never-used SubscriptionStatus::is_cancelled (registry.rs:93), SubscriptionCadence::as_str (registry.rs:107), and SubscriptionPricing::as_str (registry.rs:124). cargo test still compiles and passes. Impact: every other agent's just check fails at clippy until this epic wires the registry up (ls.2.1.2 is closed but has no commit on master yet; ls.2.1.3 is in progress), or the symbols get a temporary allow.

[2026-11-15T22:03:16Z · bob-cli-ls.2.1.land] LAND AUDIT / FOLLOW-UP TRIAGE (HEAD and fetched origin/master 055f9b6e): read this epic and every note on ls.2.1.1/.2/.3, parent phase ls.2 and outer epic ls, both linked plans, design match/import/attribution sections, and production code plus epic commits c59b5b80, 96b35f41, 055f9b6e. Decisions remain payee_source=record_title and no memory edits; outer Markdown naming is still ls.4 scope. Interleaved gcal commits ee6d6503/476c5440/d794e0ba/b638fb0d need no subscription integration; bank-config 248befdd already shares the merged CLI and config APIs, so preserve config fingerprints and located diagnostics in repairs. Old clippy note: RecordField import removed in 96b35f41; cadence/pricing/status methods now have callers, though unused re-export allowances remain for later consumers. epic-symbols currently empty and no symvision recipe. Remaining epic defects: affected_rows enriches only wanted rows against input.journal rather than the full projected journal+row after-state, drops new before_start history, and ignores current links on unaffected rows; source-free -F skips the registry entirely. Orphan ID rows enter record ledger totals; journal-only inference cannot consult config rules. Money code saturates/uses unchecked refund sum; four-weekly large representable monthly results can become zero. current_step never goes negative for future renews and caps old schedules at 240. Registry dependency guards cover album declarations but omit consulted parent/non-album bytes. Required CLI subscription parity and guarded-apply tests are missing. These stay epic work in a medium tale that must finish this epic and parent phase closeout. PROPOSED FOLLOW-UP outcomes: (1) ls.2.1.2 #2 duplicates bob-cli-g8; phase already +1ed it and 96b35f41 contains its exact bob_completion_command helper fix; added a fix-provenance note, declined a new task/duplicate vote. (2) ls.2.1.3 #1 independently reproduced via canonical count_words: bob-plugins f72bd4e=6000, lt.3 commit 63ff165=6055; mounted copy=6055. Corroborated closed bob-cli-il as post-close recurrence (prior 61c506d=5546) and routed causal DISCOVERED ISSUE to active bob-cli-lt; no new task. The unrelated docs budget failure is not subscription work. No current full-check pass is claimed.

[2026-11-15T22:05:47Z · bob-cli-ls.2.1.land] Remaining-work tale sase_plan_subscription_core_closeout.md is authored as tier=tale size=medium and passed the required explain/edit/revalidate loop with zero warnings. It specifies historical-vs-row separation, complete projected import state and source-free restore, exact guarded registry dependencies, checked money and signed timeline anchoring, command-level regressions, preservation of concurrent config-report contracts, and mandatory same-turn closeout of this epic followed by parent phase bob-cli-ls.2 only. Both child follow-ups were triaged and recorded before proposal. No production code was changed in this lander turn; no new check pass is claimed. The epic and parent phase intentionally stay open until that coder completes the repairs and gates.

[2026-11-15T22:54:09Z · bob-cli-ls.2.1.land] LAND CLOSEOUT: HEAD and origin/master remain 055f9b6e (no post-audit commits). Children bob-cli-ls.2.1.1/.2/.3 stay closed done. sase bead epic-symbols bob-cli-ls.2.1 is empty; this checkout has no just symvision recipe. Note #1 unused-registry clippy is gone: RecordField removed, status/cadence/pricing have callers; just check clippy passed with -D unused.

Repairs landed in this turn: historical ledger membership is folded journal plus uncovered ID-less typed rows; orphan IDs and covered explicit typed rows still project without entering gross/net/latest/price/timeline; journal-only classification uses config rules then builtins (TUNELY MOVE transfer exclusion; never infer income/refund from sign). Import after-state folds the existing journal with this batch's NewTxn/NewImport, overlays planned after-images, enriches the full snapshot, then selects affected/restored IDs; raw descriptors reach matching; source-free bob bank import -F always loads and guards the registry. Loader binds parent/ancestor notes, every root Markdown preimage including absents, and missing record folders. Money uses checked i128 and exact half-up; overflow emits bank_subscription_amount_overflow and suppresses the fact. current_step is a signed offset (future renews and old anchors). to_cancel marks only the latest qualifying charge; after_cancel marks every ended-rule charge with the newest as the record-level finding; refunds stay out of charge sentries and variable usage.

Verified: cargo test --lib bank::subscriptions import_plan import_run journal (including import_after_state_uses_projected_journal_and_historical_links and subscription_stale_inputs_refuse_before_import_writes); CLI Tunely/Cloudbox fixtures in tests/cli/bank.rs (preview/apply/list/report agreement, renamed media.md noun album, missing/invalid album bounds, -F restore, byte-idempotent replay, restaurant exact-title link, rule>subscription suggestion, hidden category); just check passed (cargo fmt --check, clippy -D unused, cargo test --workspace --no-fail-fast). just docs-check fails only on mounted docs/reference/plugins/bob-ledger-tools.md 6055 vs 6000, unchanged from bob-cli-lt.3 / bob-cli-il (ls.2.1.3 note #1); no plugin-doc edit and no cap raise. Follow-ups: ls.2.1.2 note #2 remains bob-cli-g8 (bob_completion_command in 96b35f41); ls.2.1.3 note #1 remains bob-cli-lt.3/bob-cli-il. No new tasks. Outer epic bob-cli-ls, plan:202611/bank_subscriptions_album.md, and bob-cli-kt stay open.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ls.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ls.2.1.land.md) | [bob-cli-ls.2.1](bob-cli-ls.2.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b8aed5a`](https://github.com/bobs-org/bob-cli/commit/b8aed5a943242a5517a6f536de9914432193ed90) | fix(bank): repair subscription core ledger, import after-state, and guards | [bob-cli-ls.2.1](bob-cli-ls.2.1.md) | 2026-11-15 17:58:47 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-lr.land][1] | Check whether the subscription registry child epic already tracks its unwired code failing clippy on master | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-lr.land/README.md

<!-- sase:referenced-by:end -->
