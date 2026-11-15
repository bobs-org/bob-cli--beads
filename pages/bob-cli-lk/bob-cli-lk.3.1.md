# Bead: bob-cli-lk.3.1 — Reopen closed Gmail Tasks on counted replies

[Bead Pages](../README.md) / [bob-cli-lk.3](bob-cli-lk.3.md) / bob-cli-lk.3.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-lk.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-lk.3.md) · **Assignee:** `bob-cli-lk.3.1.land`
**Created:** 2026-11-14 14:00:55 EST · **Closed:** 2026-11-14 21:51:41 EST
**Plan:** [202611/gmail\_closed\_reply\_reopen.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_closed_reply_reopen.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/gmail_closed_reply_reopen.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_closed_reply_reopen.md

<!-- sase:links:end -->

## Description

A counted reply or bounce after every effective Gmail linker closes saves its message, reopens the newest closed task in place or from done/, records an exact reply-card log entry, and resurfaces the task with safe retries and recovery.

## Notes

[2026-11-15T01:17:33Z · bob-cli-lk.3.1.land] LAND REVIEW: Audited epic and all four child scopes/every note, parent phase bob-cli-lk.3 DECISIONS, approved plan, child commits b112a618/78f9bdc9/88fb9cb4/ff272bc6 and current production source at ff272bc6. Completion is not yet safe: reopen recovery receipts are not consulted by build_attempt, pending_tasks receipts can strand already-open/restored targets after the write/checkpoint window, marker-only receipts can permit stale M to reapply after reclose plus log removal, and fresh turn markers are not checked before reopen edits. The pure overlay trusts stale id-less line numbers/fallbacks and does not refresh prior outcome locators after subsequent edits. Also found wrong Today input (watchers instead of ledger), report sender from stale mail index, prefix-only message-card dedupe, and obsolete dead-code allowances. These are caused by this epic and remain epic work. Preparing one medium tale for bounded repairs, regression evidence, and complete same-turn closeout; neither this epic nor parent phase is closed. Detailed source evidence: file:explicit:755288a4b63f0c4483ea2fd7. Integration reviewed non-epic 643b3697/257fec08 and 13fdf78d/719dbd45 since first child, plus concurrent outer 7ffc8251 and e221958e since creation. Archive digest-v2 stable identity remains intact; Areas changes need no Gmail wiring. Rechecked bob-plugins f68dbdc via sase repo: decoder and close notice accept additive action unchanged. epic-symbols currently empty; justfile has no symvision recipe. No runtime gates were rerun in this audit; phase verification is attributed evidence, and repair acceptance is still required. The tale must close bob-cli-lk.3.1, mark plan:202611/gmail_closed_reply_reopen.md done, verify and close parent phase bob-cli-lk.3 only, and leave outer bob-cli-lk to its waiting land agent. Follow-up outcomes are in LAND TRIAGE.

[2026-11-15T01:22:45Z · bob-cli-lk.3.1.land] LAND TRIAGE (all child PROPOSED FOLLOW-UP entries reviewed): bob-cli-lk.3.1.4 note #1 accepted as new small CI task bob-cli-lo (bank.md:210 out-of-docs Bank walk link from 643b3697 / closed bob-cli-lm.5). Same symptom class as bob-cli-l7 but independently fixable target/file, so a related link was added rather than misclassifying it as a duplicate. Source/blame and full active-epic sweep show no causal relation to Gmail or an active epic. Note #3 corroborated existing bob-cli-kl (+1, now 12 reports) with attributed monitor 9r12q4vpf4ne failure/isolated-pass evidence; declined a new duplicate task. No other child proposed follow-ups. Evidence: file:explicit:755288a4b63f0c4483ea2fd7. No just check-full run. These outcomes must be included in the eventual close note.

[2026-11-15T02:51:41Z · bob-cli-lk.3.1.land--1] Verified source at ff272bc6 with no commits beyond the audited tip; all four child phases are closed and inherited decisions remain newest effective linker, mark_unblocked with WRITE skips, exact reply-card REOPEN LOG, schema 1, and the authorized Gmail Task glossary update. Repaired reopen ownership recovery with body-free exact postimage checks and marker-last replay, fresh marker validation, and safe cursor settlement; corrected overlay identity resolution for id-less rows and shifting locators, Today membership from the ledger, triggering reply sender in reports, and exact message-card delimiter matching. Regression coverage includes crash and recovery, edits and restores, duplicate identities, Today controls, and Bea reply attribution. Verification passed: just docs-gen; just docs-check (447 passed, 1 skipped; all documentation gates); just check (Clippy, 7039 library tests, 3653 CLI tests, and all remaining suites; 3 library tests ignored). epic-symbols is empty; no symvision recipe. Follow-ups: bob-cli-kl corroboration +1 and duplicate declined; no other child proposals. Independent Bank link task bob-cli-lo was fixed, docs-checked, and closed without treating it as Gmail work.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-lk.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-lk.3.1.land.md) | [bob-cli-lk.3.1](bob-cli-lk.3.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`92f5d1c`](https://github.com/bobs-org/bob-cli/commit/92f5d1c81d93a72a26cf96c4cad8ba72fa01328e) | fix(gmail): make reply reopen recovery ownership-safe | [bob-cli-lk.3.1](bob-cli-lk.3.1.md) | 2026-11-14 21:57:34 EST |
| bob-cli--plans | [`bob-cli--plans@81221f8`](https://github.com/bobs-org/bob-cli--plans/commit/81221f8d4237102a8581b22222f6268fa97908a4) | docs(plans): mark Gmail reopen plans done | [bob-cli-lk.3.1](bob-cli-lk.3.1.md) | 2026-11-14 21:58:41 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-lk.3.1.1--1][1] | Need the epic decisions governing this phase before closure | 1 |
| read-by | [agent:bob-cli-lk.3.1.2][2] | Need parent epic DECISIONS and phase design context | 1 |
| read-by | [agent:bob-cli-lk.3.1.land--1][3] | Recheck phase status, notes, descendants and parent link before closure | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-lk.3.1.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lk.3.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-lk.3.1.land.md

<!-- sase:referenced-by:end -->
