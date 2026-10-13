# Bead: bob-cli-6u.18.7.6 — Finish ^prj project blocking — fix what the bob-cli-6u.18.7 land audit found

[Bead Pages](../README.md) / [bob-cli-6u.18.7](bob-cli-6u.18.7.md) / bob-cli-6u.18.7.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-6u.18.7.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.18.7.land.md) · **Assignee:** `bob-cli-6u.18.7.6.land`
**Created:** 2026-10-12 22:09:27 EDT · **Closed:** 2026-10-12 23:20:43 EDT
**Plan:** [202610/prj\_line\_blocking\_final\_audit\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_blocking_final_audit_fixes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/prj_line_blocking_final_audit_fixes.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_blocking_final_audit_fixes.md

<!-- sase:links:end -->

## Description

Every defect the bob-cli-6u.18.7 land audit found in the ^prj project-blocking fixes is fixed in bob-cli and bob-plugins, each with a regression test that fails on the old code. bob-cli `just check` fails only the bob-cli-6m percent-listen tests. bob-plugins `npm test` fails only the known bob-cli-6v, bob-cli-6w and bob-cli-3w cases. The fixed bob and plugins are installed on this host and, when it is reachable, on the MacBook.

## Notes

[2026-10-13T03:03:25Z · bob-cli-6u.18.7.6.land] LAND AUDIT + FOLLOW-UP TRIAGE (2026-10-13): Read all four phase scopes and every note, approved current plan, governing decisions, and actual phase commits: bob-cli 332e507/178dc21/2fcf41a, bob-plugins 7303ff4/5d8975b. Source confirms exact prj close matching, PDR7 line warnings with field-only legacy/adoption gates, configured-open project rendering, top-level capture cleanup fields and human tests, restored CRLF/PDB4/PDB6 tests, nav blocked-prj walk-through and failure-aware reversal, schedule/writer wiring tests, and cycler resolved cross-note/Cancelled/transcluded recovery with split resident and exact notice tests. One current-plan item remains: cli-fixes item 6 explicitly names resident_after_prj_before_fence_is_not_hidden_by_stale_fence_range, but it still staged.insert(1, ...) inside frontmatter (src/native/capture/project_deps.rs ~363). 2fcf41a changed the OTHER fixture resident_block_edits_idless_rows_and_rechecks_shifted_fences (~321). Correct the named fixture and mutation-check stale-context failure; this is remaining epic work, not a task. Integration: fetched both origin/master refs; all commits since the current epic first appeared (332e507 / 7303ff4), and since top epic 6u first appeared (37c100f / f47be84), belong to the epic family. No unrelated commits require integration. Checks: just check via ToolRun 53c46272e8b7922a27d0a03658ac49e5 has 2454 lib + 1414 CLI passes and ONLY the two allowed percent-listen failures; other targets pass. Plugin build unchanged, validate 6/6, npm test ToolRun 26acfb9ab36a5ebc70140e0434233742: 2561 pass / 6 allowed failures (6v x4, 6w, 3w). FOLLOW-UP OUTCOME: sole current PROPOSED FOLLOW-UP (6u.18.7.6.1 #1) duplicates bob-cli-6m; used sase_new_task, searched all-status CI tasks/recent CI sweep and active epic scopes, recorded independent +1 (now +7); no new task. Prior descendant proposals retain their recorded dispositions on 6u, 6u.18 and 6u.18.7: 6m/5l/3w/6v/6w duplicates; 6x/6y/6z/70/71/72/73 existing tasks; epic-caused fixture failures fixed as epic work; expired fixture failures and rejected cascade/relink/conditional 6t record proposals declined for reasons already recorded. 73 note #2 correctly supersedes its stale day_file contract. Host bob installed at 2fcf41a, 6 plugins synced (nav 2.27.0/cycler 1.34.0), reconcile BOB_NOW=2026-10-12 dry-run ok with no writes/warnings, projects sync dry-run 85 projects/0 edits/0 warnings. Mac remains unverified as recorded by rollout; every linked plan explicitly permits best effort and records bob-before-plugin retry/reload/pilot for Bryan, so no new coding task for offline availability. Reviewed all 32 phase notes across four epic levels and each prior land note; pending source fix is the only new blocker. All four epic-symbol audits empty; no symvision recipe in either current Justfile. Linked-plan readiness scan finds no errors for these four plan files (legacy errors elsewhere do not govern them); authoring-only plan validation rejects accepted system decision metadata on older plans, which must be preserved. Will propose a small tale whose final step closes its own bead, this epic, and ready directly parented epic ancestors in the same coding turn, then marks the four linked plans done.

[2026-10-13T03:20:43Z · bob-cli-6u.18.7.6.land] LAND CLOSE (2026-10-13): Remaining named fixture is corrected. `resident_after_prj_before_fence_is_not_hidden_by_stale_fence_range` now finds the `^prj` index and inserts the tab-indented Depends-On child at `prj_index + 1` (was `staged.insert(1, ...)` inside YAML frontmatter). Frontmatter/`^prj` stay recognised after the insert. Resident-before-fence scenario, tag/edit assertions, and unedited fenced example remain.

Mutation proof: with production `plan_resident_block` using rebuilt `staged_context.is_resident`, the named test passed. Temporarily using incoming `context.is_resident` failed (`residents` left `[]` vs `["resident"]` — stale fence range covered the shifted resident). Restored production code; test passed again. Final diff is test-only.

All four phases remain closed and were rechecked against their commits: bob-cli `332e507` / `178dc21` / `2fcf41a`, bob-plugins `7303ff4` / `5d8975b`. Honoured decisions: `tag_scope = every_resident`, `unblock_keeps = yes`, `direct_prj_link = raise`.

Verification: `cargo test --lib resident_after_prj_before_fence_is_not_hidden_by_stale_fence_range` ok after restore. `sase tool run -- just check` ToolRun `dba32cc705a15d2ea4eafe67e4e4a728` failed/101 with 2454 lib pass, 1414 CLI pass, and only the allowed bob-cli-6m pair (`percent_listen_reference_runs_existing_worker_and_installs_audio`, `failed_percent_listen_worker_keeps_listen_retry_guidance`). Other targets passed. No plugin source change this tale.

Integration: fetched origin/master; bob-cli commits since `332e507` are `178dc21` and `2fcf41a`; plugins since `7303ff4` is `5d8975b`; every commit since `37c100f` / `f47be84` still belongs to the 6u family. No unrelated commits.

Follow-up: phase `.1` note #1 remains a duplicate of bob-cli-6m; independent +1 already recorded, no new task. Prior ancestor proposal outcomes on 6u / 6u.18 / 6u.18.7 preserved (6m/5l/3w/6v/6w duplicates; 6x/6y/6z/70/71/72/73 existing tasks; cascade/relink/conditional 6t declined).

`sase bead epic-symbols bob-cli-6u.18.7.6` empty. No `just symvision` recipe. Linked tale plan `plan:202610/prj_fenced_fixture_and_closeout.md` marked done. Mac remainder unchanged: host bob `2fcf41a`, six plugins synced (nav 2.27.0, cycler 1.34.0, block-id-prompt 1.29.0, ledger-tools 1.49.0, project-tasks 1.0.0, vim-surround 1.5.2), reconcile/projects-sync dry-runs already passed with `BOB_NOW=2026-10-12`; Mac unverified/offline; retry/install/bob-before-plugin/reload/pilot stay on `bob-cli-6u.18.7.6.4`. No live reconcile or projects sync run. Previous land audit note preserved as evidence.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.18.7.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.18.7.6.land.md) | [bob-cli-6u.18.7.6](bob-cli-6u.18.7.6.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`08d9e1f`](https://github.com/bobs-org/bob-cli/commit/08d9e1f054db96f2351e483d61547d6e36af395a) | test(capture): insert Depends-On after ^prj in fenced-index fixture | [bob-cli-6u.18.7.6](bob-cli-6u.18.7.6.md) | 2026-10-12 23:24:15 EDT |
| bob-cli--plans | [`bob-cli--plans@2fb610c`](https://github.com/bobs-org/bob-cli--plans/commit/2fb610c8afd6ebf971e8362f042217424b73a532) | docs(plans): mark project-blocking landing chain done | [bob-cli-6u.18.7.6](bob-cli-6u.18.7.6.md) | 2026-10-12 23:25:14 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-6u.18.7.6.2][1] | need epic decisions and design | 1 |
| read-by | [agent:bob-cli-6u.18.7.6.3][2] | Need parent epic DECISIONS for cycler-fixes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.18.7.6.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.18.7.6.3/README.md

<!-- sase:referenced-by:end -->
