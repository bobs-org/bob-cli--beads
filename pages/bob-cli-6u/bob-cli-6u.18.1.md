# Bead: bob-cli-6u.18.1 — Reconcile and close-path fixes plus the two epic-caused CLI test failures

[Bead Pages](../README.md) / [bob-cli-6u.18](bob-cli-6u.18.md) / bob-cli-6u.18.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-6u.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.land.md) · **Assignee:** `bob-cli-6u.18.1` · **Size:** medium
**Created:** 2026-10-12 18:07:06 EDT · **Closed:** 2026-10-12 18:58:52 EDT
**Plan:** [202610/prj\_line\_blocking\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_blocking_landing_fixes.md)

## Description

cli-reconcile-close: fix the two failing CLI fixtures, strip #prj_is_blocked from every resident when ^prj recovers (PDC3), guard internal ^prj targets on the adoption/legacy paths, stop marking status-only flips structural, recurring and CRLF fixes, the direct-link ^prj rule, dead code, and missing reconcile tests.

## Notes

[2026-10-12T22:58:19Z · bob-cli-6u.18.1] PROPOSED FOLLOW-UP: capture::r#ref percent-listen CLI tests still fail identically on this tree — failed_percent_listen_worker_keeps_listen_retry_guidance and percent_listen_reference_runs_existing_worker_and_installs_audio — tracked by epic bob-cli-6m; just check is otherwise green.

[2026-10-12T22:58:34Z · bob-cli-6u.18.1] Vault dry-run: `cargo run --offline --quiet -- task reconcile --dry-run -f json` (BOB_DIR defaulted to ~/bob). ok=true, dry_run=true, daily_file=2026/20261012.md, previous_daily_file=2026/20261011.md, scanned_files=5108, open_pomodoros=2, references=7. No planned writes: marked_next/in_progress/cleared/marked_blocked/unblocked all empty; struck/moved/consumed/duplicates/empty-pomodoros all empty; grouping empty; applied_files/deferred_files empty; dependency_projection_updates/adopted/healed/canonicalized empty; dependency_warnings empty; prj_is_blocked_tags_added/stripped empty; unblocked_fields_written/pruned empty. kept_next=3, kept_in_progress=4 (sticky lanes, no rewrite). plan_budget status=ok (themes 2/4, links 7/12, next 3/15, pending 9/10). Nothing non-trivial to explain: the live vault already matches the line-model reconcile.

[2026-10-12T22:58:52Z · bob-cli-6u.18.1] Verified cli-reconcile-close: schedule.rs + blocked.rs fixtures match ^prj blocking; PDC3 strips #prj_is_blocked from leftover open residents on recovery and successor close; PDR7 internal-target guard on accepted/legacy/adoption plus same-note id filter on sync/close blocking; status-only flips skip the quiet period; shared is_recurring_task_line for UB5; recovery.rs preserves CRLF; direct_prj_link=raise (ADJ-11 only for dep edges); tag-add counts real additions; empty-pomodoro line-number docs; dead code removed. CLI blocked+schedule 23/23, recovery 10, successor 30, sync 36, structure 33. just check: lib green; CLI fails only bob-cli-6m percent-listen pair. Vault dry-run against ~/bob planned no writes. epic-symbols: none.

## Dependencies

- **Blocks:** [bob-cli-6u.18.2](bob-cli-6u.18.2.md) ◐ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.18.6](bob-cli-6u.18.6.md) ◐ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.18.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.18.1/README.md) | [bob-cli-6u.18.1](bob-cli-6u.18.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`54ac68b`](https://github.com/bobs-org/bob-cli/commit/54ac68b25bbb3aef070c817f55dfbe56e620f4bf) | fix(tasks): land prj-line reconcile and close-path defects | [bob-cli-6u.18.1](bob-cli-6u.18.1.md) | 2026-10-12 19:22:05 EDT |
