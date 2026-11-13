# Bead: bob-cli-lc.8 — Weekly guide, contract docs, memory, and the trial

[Bead Pages](../README.md) / [bob-cli-lc](README.md) / bob-cli-lc.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1c7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1c7.md) · **Assignee:** `bob-cli-lc.8` · **Size:** medium
**Created:** 2026-11-13 10:55:28 EST · **Closed:** 2026-11-13 15:23:00 EST
**Plan:** [202611/bank\_weekly\_category\_walk.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_weekly_category_walk.md)

## Description

wrapup: rewrite the bank guide for the weekly walk, note the card in docs/bank.md ownership, prove the real vault end to end with counts only, apply the memory and kv decisions, and record the 2–4 week trial as a proposed follow-up.

## Notes

[2026-11-13T20:22:08Z · bob-cli-lc.8] kv_snooze = hold: the bob-cli-kv bank-feed spike stays snoozed; the 2-4 week Category-card walk trial informs whether a feed is still needed on 2026-12-14. No unsnooze, no bead filed.

[2026-11-13T20:22:20Z · bob-cli-lc.8] PROPOSED FOLLOW-UP: 2-4 week Category-card walk trial review. Review the trial with Bryan and decide whether a bank feed is still needed (informs bob-cli-kv on 2026-12-14): the share of acknowledged rows carrying a category; the no-category rate and the correction rate (Bank: set category use, from Bryan); weekly import continuity from the journal bank.import events; whether most filings accepted the suggestion with Enter (if so, consider skip-when-suggested); whether to show suggestion chips on waiting rows.

[2026-11-13T20:22:39Z · bob-cli-lc.8] PROPOSED FOLLOW-UP: pre-existing check failures reproduce on the clean base tree and are not from this phase (docs-only change: guide rewrite + bank.md Ownership/ritual lines). (1) just check: lib test native::gcal::cli::tests::sync_args_read_last_n_days_aliases_and_default_to_none fails identically with my docs edits stashed; already tracked via bob-cli-l5.3.1.1 / bob-cli-l5.3.1.3 notes. (2) just docs-check: reference budget errors on generated docs/reference/plugins/bob-ledger-tools.md (6115 words) and bob-navigation-hotkeys.md (6019, cap 6000), sourced from bob-plugins and untouched by this phase; already noted on bob-cli-ld.7. (3) subprocess_runner raw_run_bounds_pipe_drain test failed once in the full run but passed on clean-tree retry: flake. Closing anyway per phase rule.

[2026-11-13T20:23:00Z · bob-cli-lc.8] Wrapup done and verified. Docs: rewrote docs/guides/acknowledge-bank-transactions.md for the weekly walk (Monday download+import with && rm, Category-card filing keys, mid-week glance, lapse catch-up with tick-only bulk + set category, category editing, chips, degraded-card note; 1056 words, URL kept); docs/bank.md Ownership now notes the card files Bryan's editor edit in one transaction, intro says Weekly ritual. Real-vault proof (counts only): bob bank check 0 errors + 1 coverage-gap warning; list -a JSON 7 rows / 0 waiting, 25 categories (24 visible all with hotkeys, 1 hidden; Everyday 12 / Bills 8 / Money moves 4); one open weekly Bank chore scheduled Mon 2026-11-16, daily occurrence done with ^acknowledge-bank intact; deployed plugins carry claimRowClose/setCategory/bank-set-category and recordJump. Memory: glossary:bank-row sentence already landed verbatim (lc.6), sase memory init clean; no decisions edits. Gates: docs-check shows only the 2 pre-existing generated-plugin budget errors; just check 2 failures both pre-existing/flake, gcal one reproduced on stashed clean tree (tracked) and subprocess one passed on retry. kv_snooze=hold + trial PROPOSED FOLLOW-UP + failure PROPOSED FOLLOW-UP recorded as bead notes. No epic symbols.

## Dependencies

- **Depends on:** [bob-cli-lc.1](bob-cli-lc.1.md) ✓ · ⧖ 2026-11-13
- **Depends on:** [bob-cli-lc.7](bob-cli-lc.7.md) ✓ · ⧖ 2026-11-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-lc.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-lc.8/README.md) | [bob-cli-lc.8](bob-cli-lc.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9c53b8d`](https://github.com/bobs-org/bob-cli/commit/9c53b8d8ae975f86bf7be969d633ec03928c39e7) | docs(bank): rewrite acknowledge guide for the weekly Category-card walk \[bob-cli-lc.8\] | [bob-cli-lc.8](bob-cli-lc.8.md) | 2026-11-13 15:25:42 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-lc.8][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-lc.8/README.md

<!-- sase:referenced-by:end -->
