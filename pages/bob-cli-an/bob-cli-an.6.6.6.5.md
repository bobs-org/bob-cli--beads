# Bead: bob-cli-an.6.6.6.5 — Backlog batch 5: Highlights quote and marker render, Pomodoro name reuse, completed-link dedupe, and Mac scan CI

[Bead Pages](../README.md) / [bob-cli-an.6.6.6](bob-cli-an.6.6.6.md) / bob-cli-an.6.6.6.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.land`
**Created:** 2026-10-24 07:37:07 EDT · **Closed:** 2026-10-24 09:29:22 EDT
**Plan:** [202610/backlog\_batch5\_highlights\_render\_pomodoro\_name\_duplicate\_link\_mac\_ci.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch5_highlights_render_pomodoro_name_duplicate_link_mac_ci.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/backlog_batch5_highlights_render_pomodoro_name_duplicate_link_mac_ci.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 5 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch5_highlights_render_pomodoro_name_duplicate_link_mac_ci.md

<!-- sase:links:end -->

## Description

Close five prioritized task beads. Stop Highlights from dropping quoted lines that look like headings and from rendering the page-1 marker as an annotation, keep completed multi-word Pomodoro names when the link form reuses them, stop completed-reference relocation from duplicating a Task Link already in the destination Pomodoro, and make bob-mac-capture RefsLibrary scan tests record ref scan argv again. The lander continues the backlog through further epics of at most five phases and five task beads until every project task bead is closed.

## Notes

[2026-10-24T13:29:22Z · bob-cli-an.6.6.6.5.land] LANDING (bob-cli-an.6.6.6.5.land, 2026-10-24). VERIFIED: read the epic and plan, all 5 phases and their notes (zero PROPOSED FOLLOW-UP entries), the commits (bob-cli 215d93c7, bff7bc72, adb9c324, ae025fd0; bob-plugins 0dbd767; bob-mac-capture 6d41b2e), and the source. Decision highlight_id_on_quote_fix=remint honored: live vault commit deae6fd9 reminted both quote ids and tombstoned the old ones. Per-task evidence: ba (closed earlier by bob-cli-bd.1; lander note added): both live quotes keep the '# ' line with no Comment. 4r closed: fresh-build live dry-run gives note_action=update for the only two leaking color-grouped notes (2->1, 1->0); a scratch real sync drops the phantoms with no tombstone, keeps genuine h-e2d9e4fa6422, and resyncs as a no-op; page-marker leak recount is 0 of 86. bb (closed earlier by bob-cli-bc.1; lander note added): the exact isolated link-form repro creates 'DEEP WORK'. 2l closed: isolated reconcile repro leaves one marked struck link, the flag-reverted build duplicates it, and the plugin cycler test passes 24/24. b7 closed: CI 40095658827 on 6d41b2e runs 2938 tests and the three RefsLibraryTests pass. Caveat: earlier diagnostics used a stale workspace target/debug/bob (Oct 18); every result above comes from the CARGO_TARGET_DIR build. INTEGRATION: non-epic commits since start are 6ec2f16a (bd.1 level-aware page headings, absorbed ba), b7645d17 and 94591ea6 (bd sections), and 5c9cfda1 (bc themes). No duplicate quote logic: bd.1 built on 215d93c7, and ref show sections keep mirror exclusion. Lander changes: removed 215d93c7's non-hermetic test live_vault_heading_shaped_quotes_stay_in_quote_when_present (hard-coded /home/bryan/bob, would break on vault edits; bd.1 fixtures cover both repros); added CLI regression task_status_hooks_drops_carried_link_already_in_completed_fallback, because the phase's unit test exercised only capture retirement (proven to fail with the reconcile flag reverted). Considered and declined: making is_quote_continuation_line level-aware after bd.1 (vault scan shows 0 mixed-level sidecars; theoretical). CHECKS: just check fmt+clippy pass; 5445 tests pass, 2 fail: tests/cli/highlights/continuations.rs::continuation_scan_tucks_two_pages_and_is_idempotent and ::continuation_scan_reports_dangling_marker. Bisected to bd.1 6ec2f16a (pass at bff7bc72, fail at 6ec2f16a); master CI 40095684849 is red on exactly these. Recorded as a DISCOVERED ISSUE on active epic bob-cli-bd, which owns it; not caused by this epic. FOLLOW-UPS: created bob-cli-be (ci, large): three CapturePanelModelTests submit-argv failures on bob-mac-capture CI, present since 54131b1 (closed batch 4), unowned. Created bob-cli-bf (bug, medium): color-grouped sidecars cut hard-wrapped quotes (linked_page_style gate); live repro remote_sase_agents_consolidated. The bd.1 PROPOSED FOLLOW-UPs (decision strand, glossary term) belong to bob-cli-bd's lander and were not triaged here. epic-symbols: none; no symvision recipe.

[2026-10-24T13:34:38Z · bob-cli-an.6.6.6.5.land] CONTINUATION (2026-10-24): commits bob-cli 8ba5f8d7 (reconcile dedupe CLI regression; non-hermetic live-vault test removed) and plans 2b31408 (batch 5 status done), both pushed. bob-plugins and bob-mac-capture unchanged by the lander. Fresh enumeration: 127 unresolved (123 ready; 4 snoozed: 3o, 6q, aa, ah). Successor epic scratch sase_plan_backlog_batch6_color_quote_walk_blocks_shift_promotion_race_mac_panel_ci.md validated with 0 warnings, parent_bead bob-cli-an.6.6.6.5. It owns bf (color-quote-wrap), 94+95 (blocks-shift-indexes), 79 (promotion-anchor-race, after blocks-shift-indexes), and be (mac-panel-argv-ci). One decision: color_grouped_quote_id, default remint. The plan copies the continuation contract. Proposing next.

[2026-10-24T16:27:40Z · bob-cli-an.6.6.6.5.6.land--2] POST-BATCH-6 READINESS RECHECK (2026-10-24): 10 descendants; batch-5 quote-boundary, mirror suppression, name reuse, completed-link dedupe, and RefsLibrary scan evidence remain covered by the integrated quote/hooks/plugin suites and Mac 9759771 CI. Follow-ups be and bf are now verified closed. All descendants closed, linked-plan schema valid, named phase count matches closed phases, plan already status done, and no epic-symbol entries. Fresh global links validation has 64 legacy errors, none affecting campaign plans. No remaining batch-scope blocker found. Preserve closed/done normally; no force. Campaign remains ongoing with 124 unresolved tasks and bounded batch 7 being proposed from an.6.6.6.5.6. No symvision recipe is available.

[2026-10-24T16:27:45Z · bob-cli-an.6.6.6.5.6.land--2] POST-BATCH-6 READINESS RECHECK (2026-10-24): 10 descendants; batch-5 quote-boundary, mirror suppression, name reuse, completed-link dedupe, and RefsLibrary scan evidence remain covered by the integrated quote/hooks/plugin suites and Mac 9759771 CI. Follow-ups be and bf are now verified closed. All descendants closed, linked-plan schema valid, named phase count matches closed phases, plan already status done, and no epic-symbol entries. Fresh global links validation has 64 legacy errors, none affecting campaign plans. No remaining batch-scope blocker found. Preserve closed/done normally; no force. Campaign remains ongoing with 124 unresolved tasks and bounded batch 7 being proposed from an.6.6.6.5.6. No symvision recipe is available.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.land/README.md) | [bob-cli-an.6.6.6.5](bob-cli-an.6.6.6.5.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8ba5f8d`](https://github.com/bobs-org/bob-cli/commit/8ba5f8d78347698df9667ac9dfd186ace1275a05) | test: cover reconcile completed-fallback dedupe and drop live-vault sidecar test | [bob-cli-an.6.6.6.5](bob-cli-an.6.6.6.5.md) | 2026-10-24 09:30:10 EDT |
| bob-cli--plans | [`bob-cli--plans@2b31408`](https://github.com/bobs-org/bob-cli--plans/commit/2b31408a05bef2949a1f5e80cef0de23e309eb35) | chore(plans): mark backlog batch 5 epic done | [bob-cli-an.6.6.6.5](bob-cli-an.6.6.6.5.md) | 2026-10-24 09:31:07 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.4][1] | Need parent epic plan and design | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.5--2][2] | Confirm the phase ancestor was left unclosed | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.land][3] | Parent traversal after batch-7 landing: confirm status, plan, and parent link | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.land--2][4] | Recheck direct parent previous landing notes and linked-plan readiness after batch 6 | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.land][5] | Need the epic scope, children, and linked plan file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.5.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.land.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.land.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.land.md

<!-- sase:referenced-by:end -->
