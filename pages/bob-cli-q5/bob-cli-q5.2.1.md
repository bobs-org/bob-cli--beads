# Bead: bob-cli-q5.2.1 — Snoozed reader integrations for bob-cli-q5.2

[Bead Pages](../README.md) / [bob-cli-q5.2](bob-cli-q5.2.md) / bob-cli-q5.2.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.2.md) · **Assignee:** `bob-cli-q5.2.1.land`
**Created:** 2026-11-25 19:37:40 EST · **Closed:** 2026-11-26 07:40:06 EST
**Plan:** [202611/snoozed\_planned\_today.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snoozed_planned_today.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/snoozed_planned_today.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snoozed_planned_today.md

<!-- sase:links:end -->

## Description

Snoozed tasks survive reconciliation without propagation, stay out of review walks, and appear in plan forecasts and schema-1 agenda output while Today remains ledger-derived; verify and close the delegated bob-cli-q5.2 phase.

## Notes

[2026-11-26T09:01:01Z · bob-cli-q7.land] DISCOVERED ISSUE (bob-cli-q7 land): walks::snoozed_planned_today_vectors_agree_across_freshness_walks_and_plan fails deterministically on bob-cli master 8ee8d03c, both in full just check and alone (cargo test -p bob-obsidian --test cli -- walks::snoozed_planned_today_vectors..., 0.41s): tests/cli/walks.rs:746 SP4 expects state ready but the freshness row reports ignored (date 2026-11-17, jobs.md ^job, reason ready). The test arrived with b8678657 (SASE_BEAD bob-cli-q5.2.1.2), whose note #3 says full executable verification was still pending.

[2026-11-26T11:09:54Z · bob-cli-q5.2.1.land] LAND FOLLOW-UP TRIAGE (all PROPOSED FOLLOW-UP entries, after /sase_new_task duplicate search, last-week sweep, and active-epic review):
1. bob-cli-q5.2.1.1 #1 stale bob-plugins docs inventory: DECLINED as resolved. Opened the linked repo through /sase_repo; untouched HEAD 3af803f9 passes npm run docs:inventory:check and git status is clean. No plugin edits or new task.
2. bob-cli-q5.2.1.1 #2 manual_contains: DECLINED as resolved by 71f7b670. Inspected its actual diff and current tests/cli/capture/complete_block_id.rs:292, now ids.contains(&"dup"). Phase .1 #3's old gate blocker is obsolete.
3. bob-cli-q5.2.1.2 #1 missing predecessor recovery implementation: CONFIRMED EPIC WORK, not an unrelated follow-up. No .1 commit is reachable; b8678657 supplied shared reads/exclusions but sync's recovery_status and daily Next keep never use snoozed. This remains in the repair tale, including the missing focused tests/help.
4. bob-cli-q5.2.1.2 #5, .3 #1, and .4 #1 broad baseline failures: consolidate the same 98-node comparison (43 lib/55 CLI; every name and normalized diagnostic matches clean base 1c23bce7, evidence file:explicit:0bc82d5d4b7f7164deb53e4c). Routed 80 drawer-cutover nodes to active bob-cli-ph and 17 settlement nodes to active bob-cli-q4 with proposing-bead attribution. Corroborated WISPr duplicate bob-cli-q9 (+4). No new umbrella or duplicate task.
5. bob-cli-q5.2.1.3 #2 hooks Alpha grouping mismatch: DECLINED as a distinct new task; task_status_hooks::sync::task_status_hooks_groups_area_project_tasks_after_final_statuses is already one of q4's 17 settlement nodes and its landing repair. Included explicitly in the q4 note.
6. Epic note #1 SP4 failure: RESOLVED in bbcae8e0, separating ignored state from ready/already_linked reason. Reviewed fixtures and assertions; phase .2 #5/#6 reports the rebuilt seven additions passing. No fresh full check is claimed by this lander.
All non-epic proposals are resolved or routed. No new task bead was needed. Keep this epic and parent phase q5.2 open until the remaining-work tale finishes their concrete closeout.

[2026-11-26T11:10:29Z · bob-cli-q5.2.1.land] LAND VERIFICATION / REMAINING WORK at f32e774c (fetched origin/master identical): read this epic's note, all four child scopes and every note, approved child and outer plans, final parent phase DECISIONS, and governing decision records. Reviewed actual reader/classifier, freshness overlays/placement/seed, walks, plan report paths/clock policy, schema-1 agenda/history, core wake planning, and epic commits b8678657/bbcae8e0/4a812173/f32e774c. Reviewed non-epic history since pre-creation 19e7fe54 and since first epic commit: q8 tie reconciliation/capture, ph drawer cutover, q4 note placement/settle acceptance, q7 caret docs, and q5.3 capture grammar/mutation/completion. Existing relation folding and settle pipeline must stay intact; actual capture-created snoozed rows need cross-command regression coverage.

Confirmed gaps prevent closing: (A) .1 recovery never landed: sync computes snoozed only for freshness WRITE skips, not recovery_status or daily Next keep. (B) plan_budget_for_sync returns None before enrichment for a Snoozed-only note. (C) shared read::ledger_identities treats prose block-link mentions as live despite Today's dedicated-link rule; core plan::live_identities additionally scans nested descendants, so align read/wake membership while preserving writer identity mappings/cleanup. Isolated installed-bob 0.6.0 corroboration (not an exact-source build) clears a daily Next and unblocks a snoozed task to Ready; a prose mention gives snooze ignored/already_linked while plan Today is 0. Current source proves those paths.

Reader extraction, planned-today review exclusions, separate forecast, agenda rows and wake history are present; Today stays ledger-derived, forecast nonbinding, schema 1 retained, Ready ignored, and no plugin/Mac/memory/release scope is claimed complete. Remaining repair also completes missing recovery tests/help and tests capture+reconcile integration. A single medium tale sase_plan_snoozed_reader_landing.md passed explain/edit/revalidate with zero warnings. Its final step closes this epic, marks plan:202611/snoozed_planned_today.md done, verifies/closes only parent phase bob-cli-q5.2, and leaves q5 to its lander. Both epic-symbols queries are empty; no symvision recipe exists at this baseline. No product code changed and no fresh full gate claimed; final just check/docs-check belongs to the repair's integrated tree. Complete follow-up triage is in the preceding note.

[2026-11-26T12:40:06Z · bob-cli-q5.2.1.land] LAND COMPLETE

Implemented the remaining planned-today recovery and landing work. Task reconciliation now gives direct Snoozed membership recovery rank and daily Next grace only, keeps blocking precedence, and does not make Snoozed tasks promotion roots or expand dependency reach. Snoozed-only hooks reports now publish the same forecast as bob plan. Shared list and wake membership now uses the dedicated Today Task Link extractor while retaining the broader identity map needed by writers. Wake strikes the authored Snoozed route even when the canonical same-note Pomodoro link differs.

Added binary regressions for daily recovery, stronger recovery rank, project/inherited blockers, no prerequisite promotion, terminal/Event/ambiguous/history and duplicate-loser exclusions, dedicated-link membership variants, LF/CRLF byte preservation with second-run idempotence, and actual capture through reconcile, readers, wake, and repeat wake. The lifecycle fixture includes bold NOTES drawers. Updated hooks help and plan, dependency, and snooze contracts; regenerated the owned CLI reference.

Verification on the integrated tree:
- cargo test --test cli snoozed: 31 passed.
- cargo test --test cli capture::pomodoros_agenda: 25 passed.
- cargo test --test cli freshness::: 35 passed.
- The dedicated membership, LF/CRLF reconcile, planned-today SP vector, and new ignored/Event/ambiguous/history recovery regressions passed.
- task_status_hooks broad run passed 193 tests; its sole failure is the already tracked Alpha grouping test described below.
- just docs-gen passed.
- just docs-check passed all gates: 447 documentation tests passed, one optional font-generation test skipped.
- git diff --check passed.
- just check reached full tests after format and Clippy; it reports 43 library and 55 CLI failures, with other test binaries and doctests passing. This matches the existing 98-node clean-base comparison file:explicit:0bc82d5d4b7f7164deb53e4c and prior q5.2.1 notes. Independently reran two representative failures on the untouched starting commit f32e774c: the Alpha grouping assertion reports the same 2-open versus 1-open badge, and task_block_layout::zones_name_every_task_child_kind reports the same NOTES Authored versus Drawers classification. No changed or new diagnostics were found in the Snoozed tests.

All four child scopes and notes were re-read and their requirements are covered. Follow-up dispositions remain as already recorded: plugin docs inventory and manual_contains are resolved; the missing predecessor recovery is completed here; the 98 clean-base failures remain routed to the existing q9, q4, ph, and q7 tracks; the earlier SP4 issue remains fixed in bbcae8e0. No new task bead was needed or created. No plugin, Mac, live-vault, memory, release, version, or CHANGELOG work is claimed. epic-symbols is empty.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.2.1.land.md) | [bob-cli-q5.2.1](bob-cli-q5.2.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9778a94`](https://github.com/bobs-org/bob-cli/commit/9778a94d38d986ecb4562816d99d11aa0d3d7073) | feat(snooze): integrate recovery rows into today planning | [bob-cli-q5.2.1](bob-cli-q5.2.1.md) | 2026-11-26 07:44:10 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.2.1.3][1] | Need parent epic scope for plan-forecast | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.2.1.3/README.md

<!-- sase:referenced-by:end -->
