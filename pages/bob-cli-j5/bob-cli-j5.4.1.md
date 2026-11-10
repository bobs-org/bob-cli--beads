# Bead: bob-cli-j5.4.1 — Complete archive pairing and guarded rename-following

[Bead Pages](../README.md) / [bob-cli-j5.4](bob-cli-j5.4.md) / bob-cli-j5.4.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-j5.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-j5.4.md) · **Assignee:** `bob-cli-j5.4.1.land`
**Created:** 2026-11-09 16:44:33 EST · **Closed:** 2026-11-09 22:18:14 EST
**Plan:** [202611/archive\_pairing\_and\_rename.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/archive_pairing_and_rename.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/archive_pairing_and_rename.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | [bead:bob-cli-jg][2] | Follow-up required by the approved archive-pair performance plan after the 60-second census cache still misses all four latency targets. |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/archive_pairing_and_rename.md
[2]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-jg/README.md

<!-- sase:links:end -->

## Description

All archive consumers share one safe metadata-first binding, archive runs follow source renames with recoverable writes, and every run reports archive health.

## Notes

[2026-11-10T01:27:27Z · bob-cli-j5.4.1.land] Land review (lander bob-cli-j5.4.1.land): all 5 phases closed and verified against source and commits b97d8d4c, 0ed552a5, 0996111c, 2327590f, 03dfe6de. Follow-up triage: no child bead recorded any PROPOSED FOLLOW-UP entry, so nothing was filed through sase_new_task. Integrated tree at 03dfe6de: just check exit 0 (10249 tests, 0 failed), just docs-check passed, no epic-symbol entries for bob-cli-j5.4.1 or bob-cli-j5.4. Live read-only preview (fresh debug binary, task archive -n -f json): exit 0 preview; renames = 2026/20260528.md: done/2026/20260528_day_done.md -> done/2026/20260528_done.md; moves dev.md 12, gtd_daily.md 18, sase.md 10 (40 blocks) plus rename-only daily (0 tasks); all six health counts 0, diagnostics complete. Intervening non-epic commits (3f8c49d4, b5196709, 076fdc48, 8728fe28, 8d098e55) do not touch archive pairing or the guarded writer; no integration needed. Lander additions: test applied_rename_preserves_stats_attribution (collect_done/tests/rename.rs), CLI test archive_rename_commits_the_removed_old_path_and_second_run_is_noop (tests/cli/move_done.rs), and a corrected pair.rs module doc about census read failures. REMAINING EPIC WORK (epic-caused, violates the plan's 'retain existing read performance'): ArchivePairIndex::read_vault serially reads every note in full. Release-profile medians on the live vault (6.7k notes), pre-epic installed bob vs HEAD: capture-related 59->224 ms, capture-related -d 0 39->201 ms, ref list 165->330 ms (RefTaskIndex reads the vault twice), stats 171->247 ms (from_buffers clones every buffer). strace: capture-related opens 856 -> 7579 .md files. Planned as a tale that also performs this epic's closeout.

[2026-11-10T02:02:10Z · bob-cli-iz.land] DISCOVERED ISSUE (from the bob-cli-iz land agent): native::task_merge::tests::mg18_merge_source_with_descendant_anchor_archives_through_bound_pair fails deterministically on bob-cli master 12692ebb (3/3 reruns: cargo test -p bob-obsidian --lib mg18_merge_source_with_descendant_anchor). Panic at src/native/task_merge/tests.rs:3042 'copied links follow the bound archive, not a _done guess': the rewritten dest.md copies still read [[done/src_done#^keep]] and [jump](done/src_done.md#^keep) instead of done/custom_archive. The test landed in 6d063ff5 (bob-cli-je, 20:18 EST); eba2bd59 (this epic, 20:28 EST) then changed src/native/collect_done/pair.rs, and 03dfe6de/2327590f own the bound-pair destination and link repair. It is the only failure in just check on that tree; bob-cli-iz's gcal-only diff does not touch task_merge or collect_done.

[2026-11-10T03:03:28Z · bob-cli-j5.4.1.land] DISCOVERED ISSUE: After the fact-only parallel census and 60-second read-only cache, seven alternating release-profile runs on the live vault still miss the approved max(25 ms, 15%) regression limit for all four commands (baseline b97d8d4c; HEAD eba2bd59; every run exited 0): capture-related 58.0→140.3 ms, capture-related -d 0 36.6→120.0 ms, ref list 164.5→268.9 ms, and stats 163.1→215.7 ms. The hot-cache call paths still rebuild and resolve the full ArchivePairIndex for each read-only request; this root-cause attribution is inferred from the measurements and source review. Follow-up task bob-cli-jg was filed as required by plan:202611/archive_pair_census_perf_and_land.md, proposed by this epic, and linked to it.

[2026-11-10T03:18:14Z · bob-cli-j5.4.1.land] Land verification: all five closed phases were checked against source and commits b97d8d4c, 0ed552a5, 0996111c, 2327590f, and 03dfe6de. No phase recorded a PROPOSED FOLLOW-UP. Intervening commits 3f8c49d4, b5196709, 076fdc48, 8728fe28, and 8d098e55 needed no integration. The lander added the stats-after-rename test, CLI Git rename test, and pair.rs doc fix.

This tale stores pair facts instead of note bodies, reads the census in parallel, shares the read with RefTaskIndex, and adds the versioned read-only fingerprint cache. Parity test pair_indexes_match_across_vault_contents_and_ref_task_reads passes. Seven alternating release-profile live-vault measurements (baseline b97d8d4c / implementation HEAD eba2bd59 plus working-tree diff SHA-256 7e641ee49e002422be4e7ddafa854371e9fa0cd1cc94e5eee5d261184209288c; all exits 0) were: capture-related 58.0/140.3 ms; capture-related -d 0 36.6/120.0 ms; ref list 164.5/268.9 ms; stats 163.1/215.7 ms. All four miss max(25 ms, 15%) above baseline, so follow-up bob-cli-jg was filed as required by the approved tale, proposed by this epic, and linked here. Remaining cost is inferred to be full pair-map reconstruction and resolution on read-only calls; cache protects facts but does not avoid that work. The earlier lander medians were 59/224, 39/201, 165/330, and 171/247 ms in the same command order.

Gates: focused suites pass (collect_done 174, ref_tasks 54, capture_related 20, ref_library 108, stats 222); just lint passes. just check ToolRun e60c9685a9d0ce979d6f256f3182326f failed only native::task_merge::tests::mg18_merge_source_with_descendant_anchor_archives_through_bound_pair (6244 passed, 1 failed, 3 ignored). This exact known conflict is recorded in epic note #2: the test expects a custom archive path while the unchanged accepted follow-renames planner canonicalizes every bound noncanonical archive. No assertion or rename behavior was changed. `just symvision` is unavailable because this justfile has no such recipe; epic-symbols reports no entries for this epic or parent phase.

Live preview: fresh local-install binary from the working tree based at eba2bd59 (diff SHA-256 above), BOB_DIR=/home/bryan/bob, `task archive -n -f json`: exit 0, preview only. Rename: 2026/20260528.md, done/2026/20260528_day_done.md -> done/2026/20260528_done.md. Moves: dev.md 12, gtd_daily.md 18, sase.md 10 (40 task blocks total), plus the daily rename-only plan with 0 tasks. All six health counts are 0 and diagnostics are complete.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-j5.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-j5.4.1.land.md) | [bob-cli-j5.4.1](bob-cli-j5.4.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`eba2bd5`](https://github.com/bobs-org/bob-cli/commit/eba2bd59a6fa6fdf8e827adbda1d42c03d97519b) | test(archive): cover stats attribution and Git commit across archive renames | [bob-cli-j5.4.1](bob-cli-j5.4.1.md) | 2026-11-09 20:28:56 EST |
| bob-cli | [`d65be1c`](https://github.com/bobs-org/bob-cli/commit/d65be1ce02b66f9a08c6a31049990aa74cccca65) | perf(archive): cache pair facts for read-only consumers | [bob-cli-j5.4.1](bob-cli-j5.4.1.md) | 2026-11-09 22:24:11 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-iz.land][1] | Check whether the mg18 bound-pair archive test failure belongs to this in-progress epic | 1 |
| read-by | [agent:bob-cli-j5.4.1.4][2] | Need DECISIONS and phase details from parent epic | 2 |
| read-by | [agent:bob-cli-j5.4.1.land][3] | Need the epic scope, children, and linked plan file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-iz.land.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.4.1.4/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-j5.4.1.land.md

<!-- sase:referenced-by:end -->
