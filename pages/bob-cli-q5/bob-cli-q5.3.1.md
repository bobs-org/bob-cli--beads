# Bead: bob-cli-q5.3.1 — Capture snooze token and atomic row operations

[Bead Pages](../README.md) / [bob-cli-q5.3](bob-cli-q5.3.md) / bob-cli-q5.3.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.3.md) · **Assignee:** `bob-cli-q5.3.1.land`
**Created:** 2026-11-25 19:34:27 EST · **Closed:** 2026-11-26 06:33:25 EST
**Plan:** [202611/capture\_snooze\_token.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_snooze_token.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/capture_snooze_token.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:5bbffb8fc717828765ca25af | attached via sase artifact create --bead |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_snooze_token.md

<!-- sase:links:end -->

## Description

Capture can snooze new and existing tasks, link or drop snoozed rows safely, and complete same-day times with documented editor and JSON contracts.

## Notes

[2026-11-26T10:48:02Z · bob-cli-q5.3.1.land] LAND FOLLOW-UP TRIAGE (bob-cli-q5.3.1.land, source HEAD 292d60c0):
Reviewed every note on .1 (4), .2 (6), and .3 (2), with sase_new_task duplicate searches, recent-task sweep, and active-epic causal review.
1. q5.3.1.1 #1 manual_contains: declined as resolved by 71f7b670; complete_block_id.rs now uses ids.contains(&"dup").
2. q5.3.1.1 #2 (15 capture CLI failures): corroborated on bob-cli-q4 as DISCOVERED ISSUE, with proposing bead and exact grouping. They are the capture subset of its existing 17 settlement failures.
3. q5.3.1.1 #3 contains two distinct reports: WISPr kicker corroborated via +1 on bob-cli-q9, and september_shaped_vault_finishes_fast fail/pass evidence via +1 on bob-cli-gz. Relayed phase observations, no fresh lander test run claimed.
4. q5.3.1.2 #1 numeric-route snooze-drop editor/execution mismatch: retained as this epic's remaining work, not a standalone task. The new drop pre-pass in editor_parse.rs masks ! and recursively hits the ordinary alphabetic-route guard. Installed grammar-33 bob reproduces mode=task/body=@20261125:here while dry-run successfully returns snooze.action=drop; current source contains the same path.
5. q5.3.1.2 #2 relative rounding: routed as DISCOVERED ISSUE to outer bob-cli-q5; core parse_relative_delta rounds the offset, and q5.1 note #2 already flags that interpretation. Capture correctly reuses it. Outer q5 must reconcile shared semantics/vector/docs; no capture-only rule or duplicate task.
6. q5.3.1.2 #4 and q5.3.1.3 #1 (same 98-node baseline set): decomposed into 80 drawer-cutover nodes corroborated on bob-cli-ph, 17 settlement nodes corroborated on bob-cli-q4, and WISPr on bob-cli-q9. Clean-base evidence is phase .2 ToolRuns d9f6d1470d4fa55a51b0d07d48d1089f/549282d9b014e9ca187b04e3ed57d52c and .3 comparison at ae78dbb2; no fresh full gate claimed here.
No new task beads were needed; all distinct non-epic proposals are already resolved or owned. Implementation/handoff notes checked: the mutation adapter removed the grammar execution guard, dispatches every accepted intent, retains schema 1, refreshes final row positions after settle, and completion/docs consume the additive contract. Remaining work and final verification are specified in a medium tale; do not close yet.

[2026-11-26T10:50:48Z · bob-cli-q5.3.1.land] LAND AUDIT / REMAINING WORK at 292d60c0 (fetched origin/master matches): reviewed original and child capture plans, original parent phase q5.3 final DECISIONS, all child scopes/notes, epic commits 1b386638/ae78dbb2/712d69d9, and actual grammar/editor/dispatch/snapshot mutation/core planner/result/completion source and tests. Source honors thin-client schema 1, shared time parser, blocked refusal without dependency removal, sticky lanes, note/history retention, ledger-only Today, meeting-end completion, and post-settle row coordinates. Audited other commits since epic creation/first epic commit: tie handling/docs/lint, drawer/caret docs and fixtures, b8678657/bbcae8e0 planned-today readers, 4a812173 plan forecast, and 292d60c0 settlement acceptance. No merge conflict or competing implementation found. Add cross-feature regression coverage using actual capture-created rows in the remaining tale.

Two feature gaps prevent closure: (a) numeric-route drop editor parses as prose although strict dry-run drops the row; source mechanism and disposable installed-grammar-33 reproduction captured in file:explicit:5bbffb8fc717828765ca25af; (b) capture_complete/snooze.rs::push_candidate discards relative filter_aliases on a duplicate event minute, so a +1 query cannot find the retained 1300 event-labelled row at 12:00. (b) is source-inspected, not runtime reproduced: installed bob predates completion and workspace target/debug/bob is stale. No fresh current-tree full gate was run; tale must build current source and verify with just check/docs-check.

Prepared sase_plan_capture_snooze_closeout.md as a medium tale; first validate --explain found missing title/goal and inert epic-only parent_bead, corrected them, and revalidation passes with zero warnings. Tale carries concrete final closure of bob-cli-q5.3.1, symvision-if-available, status done in plan:202611/capture_snooze_token.md, and normal closure of parent phase bob-cli-q5.3, leaving outer bob-cli-q5 open. No step waits for its own commit/push/CI. epic-symbols currently reports no entries for q5.3.1 or q5.3; justfile currently has no symvision recipe. All external proposals were triaged in the preceding note. Epic and parent phase intentionally remain open until this bounded work and verification finish.

[2026-11-26T11:33:25Z · bob-cli-q5.3.1.land] Closeout tale 202611/capture_snooze_closeout.md implemented. Two gaps repaired: (a) numeric-route drop editor preview now uses the validated route/block/source range instead of masked re-parse, so @20261125:here! and @2026:here! report mode pomodoro_link with exact route/block/snooze spans agreeing with strict parse and dry-run, Unicode offsets preserved, numeric prose unchanged elsewhere, alphabetic drop/toggle/malformed behavior preserved; (b) capture_complete/snooze.rs push_candidate now merges relative filter aliases into the retained earliest-source candidate, so an event end colliding with +1h keeps one event-labelled 1300 row that +1/+1h still match, ordering stable, replacement stays literal HHMM, aliases absent from JSON; docs/capture.md completion paragraph updated. Reader/settlement integration: CLI plan_snoozed, walks (incl planned-today/freshness vectors), settle_acceptance (incl snooze add/drop nothing-note-local) all pass; capture snooze dry-run/real byte identity verified for numeric retime and drop with task line preserved. Tests: new lib grammar numeric_route_drop_matches_strict_parse PASS, new lib dedup alias test PASS, new CLI parse numeric drop PASS, extended CLI local_daily retime/drop PASS; suites: lib snooze 73 PASS, lib capture_language 943 PASS, CLI capture::snooze 18 PASS, CLI plan/walks/settle 46 PASS. Baseline failures attributed, none new in scope: lib capture_complete 24 FAIL all drawer/routes_tasks pre-existing drawer cutover owned by bob-cli-ph (one representative re-ran on clean base and fails identically); CLI capture:: suite 2063 PASS / 46 FAIL all drawer-related, zero snooze failures, same drawer baseline; clippy gate passes with pre-existing warnings; fmt clean; docs-check lint ok and contract content current but recipe FAILs on stale plugin inventory docs/bob-ledger-tools.md and docs/index.md unrelated to this change (needs plugin-side docs gen). Follow-ups from land triage (no duplicates created): q5.3.1.1 #1 manual_contains resolved by 71f7b670 declined; #2 15 capture fixture failures DISCOVERED ISSUE corroboration on bob-cli-q4; #3 WISPr kicker +1 on bob-cli-q9 and agenda flake +1 on bob-cli-gz; #2 numeric drop retained as this epic work now done; #2 relative rounding DISCOVERED ISSUE on outer bob-cli-q5 (core parse_relative_delta shared rule, outer must reconcile wording/vectors/docs, no capture-only rule); #4 and q5.3.1.3 #1 same 98-node set decomposed to 80 drawer nodes bob-cli-ph, 17 settlement nodes bob-cli-q4, WISPr bob-cli-q9. No new task beads. just symvision has no recipe in this justfile; unavailability recorded, no pass claimed. No commit/push/CI waited on.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.3.1.land.md) | [bob-cli-q5.3.1](bob-cli-q5.3.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`7048c5c`](https://github.com/bobs-org/bob-cli/commit/7048c5c489ebadcb577ad1281a4c3fb85c2190de) | feat(capture): finish snooze drop preview parity and completion alias merge | [bob-cli-q5.3.1](bob-cli-q5.3.1.md) | 2026-11-26 06:35:24 EST |
