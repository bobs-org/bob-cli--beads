# Bead: bob-cli-j5 — Fix done-notes archiving without changing the done/ layout

[Bead Pages](../README.md) / bob-cli-j5

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ai](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ai.md) · **Assignee:** `bob-cli-j5.land`
**Created:** 2026-11-09 11:04:08 EST · **Closed:** 2026-11-10 02:30:34 EST
**Plan:** [202611/done\_notes\_archiving\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/done_notes_archiving_fixes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/done_notes_archiving_fixes.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | [bead:bob-cli-jh][2] | Found by bob-cli-j5's land agent during the restore phase's audit of in-place reopen writers; bob task restore -r is the sanctioned way to reopen an archived task |
| related | file:explicit:82c6a707ddd506f8b0f9d403 | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/done_notes_archiving_fixes.md
[2]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-jh/README.md

<!-- sase:links:end -->

## Description

`bob task archive` moves only what it should, from notes that should feed done/, at a predictable time, through a writer as safe as `bob task move`. Archive pairing survives renames, every Bob path check agrees on what done/ means, and an archived task can come back with one command or one plugin gesture.

## Notes

[2026-11-10T03:22:59Z · bob-cli-j8.3.1.land] DISCOVERED ISSUE: Independent reproduction in the approved notebook-capture workspace: cargo test --lib mg18_merge_source_with_descendant_anchor_archives_through_bound_pair -- --nocapture exits 101 with only that test failing (6,248 filtered). The test expects its fixture's done/custom_archive destination, but copied links remain on done/src_done; source: src/native/task_merge/tests.rs:3042. Neither task_merge nor collect_done is changed by this notebook work. Durable reproduction: file:explicit:82c6a707ddd506f8b0f9d403. This corroborates the already-recorded custom archive pairing issue; no new task bead filed.

[2026-11-10T06:53:31Z · bob-cli-j5.land] FOLLOW-UP TRIAGE (bob-cli-j5.land): Reviewed every PROPOSED FOLLOW-UP on phases j5.1-j5.8 and nested epics j5.2.1 and j5.4.1.
(1) j5.1 #1, Mac capture page word budgets: already tracked by bob-cli-h9 and corroborated by bob-cli-j5.2.1.land. No second +1 from this epic.
(2) j5.3 #3/#4, json-outputs.md over budget (6143): obsolete. The page is now 5995 words (cap 6000) after 527f30ad/4a0206ec. j5.2.1.land had routed it to bob-cli-j8. No task.
(3) j5.5 #1 and j5.6 #2, mg18 bound-archive test: resolved in-epic by 15a79998, which aligned the test with the accepted canonicalizing rename. It passes on 6a7afcd2 and in the full just check (10331 passed, 0 failed). No task.
(4) j5.5 #2, j5.6 #1, j5.8 #1, docs-check bob-mac-capture mount index collision: semantic duplicate of bob-cli-jf. Root cause: bob-mac-capture master is still 9a0bb25c, and the bob-docs cache holds bob-cli's tree. Recorded a +1 on bob-cli-jf. It is not bob-cli-it, which covers a stale gitignored index.
(5) Restore-phase reopen-writer audit (plan step 5, never recorded by j5.6): done by the lander. gcal refile, highlights_ref, task_move restore, and successors are safe. The only finding is capture plan_promotions reopening closed or done/ prerequisites in place; it predates the epic (bob-cli-6u.8) and is filed as bob-cli-jh (small bug, ready).
(6) bob-cli-jg, archive pair-index latency: epic-caused, but the approved archive_pair_census_perf_and_land plan made it a separate task linked to j5.4.1. It stays its own ready task.
(7) j5.3 notes #1-#2 are stray non-proposals.
bob-cli-em stays out of scope per the plan.

[2026-11-10T06:55:32Z · bob-cli-j5.land] LAND AUDIT (bob-cli-j5.land): Checked all eight phases and nested epics j5.2.1/j5.4.1 against source and commits f1ee393d..6a7afcd2, plus bob-plugins 16c0454. Selection, guarded writer, link repair, pairing, restore, path contract (no leftover Rust done/ shapes), and plugins (vectors sha 9b9ce16d pinned in all four plugins; reopen via restore -o -r -f json) match the plan and DECISIONS. No memory or version edits.
Intervening commits needed no integration: task-merge 076fdc48/6d063ff5 (mg18 aligned in 15a79998), notebooks (snapshot uses skip_archive_directory), gcal (daily notes only), docs 527f30ad/4a0206ec.
Gates on 6a7afcd2: just check 10331 passed, 0 failed; just docs-check fails only on the bob-cli-jf mount collision.
Live read-only preview: 37 sources, 151 roots, 1 rename, 0 holds, all health counts 0.
REMAINING EPIC WORK (keep-window phase j5.5 shipped part of the week_cap decision): hard-coded 7/10 with no archive.keep_days/archive.keep_max config; no per-note archive_keep N|off; undated roots stay instead of moving as oldest under ## Undated; a missing month heading is always appended rather than placed chronologically. Proposed a medium tale (sase_plan_finish_archive_keep_window_and_land_j5) that finishes these gaps and then closes this epic. bob-cli-j5 has no parent_bead. Epic-symbols empty. The justfile has no symvision recipe.

[2026-11-10T07:30:34Z · bob-cli-j5.land] Land verification: all eight phases (selection, guarded writer incl. nested epic j5.2.1, link repair, pairing incl. nested epic j5.4.1, keep-window, restore, path contract, plugins) checked against source and commits f1ee393d..6a7afcd2 plus bob-plugins 16c0454. DECISIONS honored (week_cap, frozen, rename, restore, no memory strand). Intervening commits (task-merge 076fdc48/6d063ff5, notebooks 0a74731b..ab021e2d, gcal d3f022a4/8ad8e270, docs 527f30ad/4a0206ec) needed no integration: notebooks use done_archive::skip_archive_directory, gcal touches only daily notes, and mg18 was aligned to canonical renames in 15a79998. Remaining keep-window gaps finished in this tale: archive.keep_days/keep_max config, archive_keep N|off, undated roots under ## Undated, chronological month headings. Gates: just check passed; docs-check blocked only by the bob-mac-capture mount collision tracked by bob-cli-jf; live read-only preview: dry_run true, exit 0, 37 selected files, 151 roots, 1 canonical rename, 0 holds, all health counts 0 (the daily-note entry was rename-only with 0 roots; obsidian.md remained grandfathered). Follow-ups: see the epic FOLLOW-UP TRIAGE note (bob-cli-jf +1, bob-cli-jh filed, bob-cli-jg and bob-cli-h9 existing, json-outputs and mg18 resolved).

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-j5.1](bob-cli-j5.1.md) | Safe archive selection | ✓ closed | medium | 2026-11-09 | 1 | 1 |
| [bob-cli-j5.2](bob-cli-j5.2.md) | Guarded archive writer with preview and JSON | ✓ closed | large | 2026-11-09 | 1 | 0 |
| [bob-cli-j5.3](bob-cli-j5.3.md) | Correct archive link repair | ✓ closed | medium | 2026-11-09 | 1 | 1 |
| [bob-cli-j5.4](bob-cli-j5.4.md) | One archive pairing resolver, rename-following, and health diagnostics | ✓ closed | large | 2026-11-09 | 1 | 0 |
| [bob-cli-j5.5](bob-cli-j5.5.md) | Keep window and month headings | ✓ closed | medium | 2026-11-09 | 1 | 1 |
| [bob-cli-j5.6](bob-cli-j5.6.md) | bob task restore | ✓ closed | medium | 2026-11-09 | 1 | 1 |
| [bob-cli-j5.7](bob-cli-j5.7.md) | One done/ path contract in bob-cli | ✓ closed | medium | 2026-11-09 | 1 | 1 |
| [bob-cli-j5.8](bob-cli-j5.8.md) | Plugin path helper and archived-task reopen | ✓ closed | medium | 2026-11-09 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-j5: Fix done-notes archiving without changing the done/ layout [closed]"]
    n1["bob-cli-j5.1: Safe archive selection [closed]"]
    n2["bob-cli-j5.2: Guarded archive writer with preview and JSON [closed]"]
    n3["bob-cli-j5.2.1: Guarded archive writer with preview and JSON [closed]"]
    n4["bob-cli-j5.2.1.1: Support recoverable creation in the guarded write engine [closed]"]
    n5["bob-cli-j5.2.1.2: Plan archive changes from captured inputs [closed]"]
    n6["bob-cli-j5.2.1.3: Apply archive plans under the lock and expose preview and JSON [closed]"]
    n7["bob-cli-j5.3: Correct archive link repair [closed]"]
    n8["bob-cli-j5.4: One archive pairing resolver, rename-following, and health diagnostics [closed]"]
    n9["bob-cli-j5.4.1: Complete archive pairing and guarded rename-following [closed]"]
    n10["bob-cli-j5.4.1.1: Build the shared archive pair index and migrate stats [closed]"]
    n11["bob-cli-j5.4.1.2: Add recoverable removals to the guarded writer [closed]"]
    n12["bob-cli-j5.4.1.3: Migrate the remaining archive readers [closed]"]
    n13["bob-cli-j5.4.1.4: Use resolved pairs in archiving and report archive health [closed]"]
    n14["bob-cli-j5.4.1.5: Follow source renames in one guarded archive plan [closed]"]
    n15["bob-cli-j5.5: Keep window and month headings [closed]"]
    n16["bob-cli-j5.6: bob task restore [closed]"]
    n17["bob-cli-j5.7: One done/ path contract in bob-cli [closed]"]
    n18["bob-cli-j5.8: Plugin path helper and archived-task reopen [closed]"]
    n0 --> n1
    n0 --> n2
    n2 --> n3
    n3 --> n4
    n3 --> n5
    n3 --> n6
    n0 --> n7
    n0 --> n8
    n8 --> n9
    n9 --> n10
    n9 --> n11
    n9 --> n12
    n9 --> n13
    n9 --> n14
    n0 --> n15
    n0 --> n16
    n0 --> n17
    n0 --> n18
    n1 -.-> n2
    n2 -.-> n7
    n4 -.-> n5
    n5 -.-> n6
    n7 -.-> n8
    n8 -.-> n15
    n8 -.-> n16
    n10 -.-> n12
    n10 -.-> n13
    n11 -.-> n14
    n12 -.-> n14
    n13 -.-> n14
    n15 -.-> n17
    n16 -.-> n17
    n16 -.-> n18
    n17 -.-> n18
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-j5.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.1/README.md) | [bob-cli-j5.1](bob-cli-j5.1.md) | 1 |
| [bbugyi200.athena.bob-cli-j5.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-j5.2.md) | [bob-cli-j5.2](bob-cli-j5.2.md) | 0 |
| [bbugyi200.athena.bob-cli-j5.2.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-j5.2.1.1.md) | [bob-cli-j5.2.1.1](bob-cli-j5.2.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-j5.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.2.1.2/README.md) | [bob-cli-j5.2.1.2](bob-cli-j5.2.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-j5.2.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.2.1.3/README.md) | [bob-cli-j5.2.1.3](bob-cli-j5.2.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-j5.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-j5.2.1.land.md) | [bob-cli-j5.2.1](bob-cli-j5.2.1.md) | 2 |
| [bbugyi200.athena.bob-cli-j5.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.3/README.md) | [bob-cli-j5.3](bob-cli-j5.3.md) | 1 |
| [bbugyi200.athena.bob-cli-j5.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-j5.4.md) | [bob-cli-j5.4](bob-cli-j5.4.md) | 0 |
| [bbugyi200.athena.bob-cli-j5.4.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.4.1.1/README.md) | [bob-cli-j5.4.1.1](bob-cli-j5.4.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-j5.4.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-j5.4.1.2.md) | [bob-cli-j5.4.1.2](bob-cli-j5.4.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-j5.4.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.4.1.3/README.md) | [bob-cli-j5.4.1.3](bob-cli-j5.4.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-j5.4.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.4.1.4/README.md) | [bob-cli-j5.4.1.4](bob-cli-j5.4.1.4.md) | 1 |
| [bbugyi200.athena.bob-cli-j5.4.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.4.1.5/README.md) | [bob-cli-j5.4.1.5](bob-cli-j5.4.1.5.md) | 1 |
| [bbugyi200.athena.bob-cli-j5.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-j5.4.1.land.md) | [bob-cli-j5.4.1](bob-cli-j5.4.1.md) | 3 |
| [bbugyi200.athena.bob-cli-j5.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.5/README.md) | [bob-cli-j5.5](bob-cli-j5.5.md) | 1 |
| [bbugyi200.athena.bob-cli-j5.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.6/README.md) | [bob-cli-j5.6](bob-cli-j5.6.md) | 1 |
| [bbugyi200.athena.bob-cli-j5.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-j5.7.md) | [bob-cli-j5.7](bob-cli-j5.7.md) | 1 |
| [bbugyi200.athena.bob-cli-j5.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.8/README.md) | [bob-cli-j5.8](bob-cli-j5.8.md) | 1 |
| [bbugyi200.athena.bob-cli-j5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-j5.land.md) | [bob-cli-j5](README.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f1ee393`](https://github.com/bobs-org/bob-cli/commit/f1ee393db4cfe49a78e75af68b3e1a5e3b5b61fd) | feat(archive): select only area and project notes for done/ | [bob-cli-j5.1](bob-cli-j5.1.md) | 2026-11-09 12:08:49 EST |
| bob-cli | [`2b5b832`](https://github.com/bobs-org/bob-cli/commit/2b5b8328777bece6483df518bada4f0b9143ff01) | feat(archive): create missing files in the guarded write engine | [bob-cli-j5.2.1.1](bob-cli-j5.2.1.1.md) | 2026-11-09 13:11:02 EST |
| bob-cli | [`37df0e5`](https://github.com/bobs-org/bob-cli/commit/37df0e52cf364c82bf5017ea8ee74d9443f66801) | feat(collect-done): snapshot inputs with exact replay and plan-wide refusal | [bob-cli-j5.2.1.2](bob-cli-j5.2.1.2.md) | 2026-11-09 14:18:18 EST |
| bob-cli | [`e802071`](https://github.com/bobs-org/bob-cli/commit/e802071f8d39039a5ae7c8b191ec456ca8557db0) | feat(archive): apply plans under the lock with dry-run preview and JSON report | [bob-cli-j5.2.1.3](bob-cli-j5.2.1.3.md) | 2026-11-09 15:10:57 EST |
| bob-cli | [`2455d9d`](https://github.com/bobs-org/bob-cli/commit/2455d9dbcaaa67936cf9b1eaaa8e842cd409422b) | fix(archive): repair guarded landing validation | [bob-cli-j5.2.1](bob-cli-j5.2.1.md) | 2026-11-09 16:06:02 EST |
| bob-cli--plans | [`bob-cli--plans@1e8d36a`](https://github.com/bobs-org/bob-cli--plans/commit/1e8d36a191d0f57d0dcceaa3c1b11c77d1d71516) | docs(plan): mark guarded archive writer done | [bob-cli-j5.2.1](bob-cli-j5.2.1.md) | 2026-11-09 16:06:34 EST |
| bob-cli | [`a846a23`](https://github.com/bobs-org/bob-cli/commit/a846a23b73a07956bdf2bd4ca0026f8d20ca2d9d) | feat(archive)!: correct archive link repair | [bob-cli-j5.3](bob-cli-j5.3.md) | 2026-11-09 16:32:51 EST |
| bob-cli | [`b97d8d4`](https://github.com/bobs-org/bob-cli/commit/b97d8d4c3b214d1f73f0627f868a108ff6755a66) | feat(archive): add recoverable removals to the guarded writer | [bob-cli-j5.4.1.2](bob-cli-j5.4.1.2.md) | 2026-11-09 17:29:23 EST |
| bob-cli | [`0ed552a`](https://github.com/bobs-org/bob-cli/commit/0ed552a5e997c30bb78dd909eea91f957e012024) | feat(archive)!: resolve archive pairs from metadata first | [bob-cli-j5.4.1.1](bob-cli-j5.4.1.1.md) | 2026-11-09 17:58:46 EST |
| bob-cli | [`0996111`](https://github.com/bobs-org/bob-cli/commit/0996111cd31bd514c23760f2c53385003a1439df) | feat(archive): migrate remaining archive readers | [bob-cli-j5.4.1.3](bob-cli-j5.4.1.3.md) | 2026-11-09 18:43:43 EST |
| bob-cli | [`2327590`](https://github.com/bobs-org/bob-cli/commit/2327590f2caabced31e6320a232d57355dfe2007) | feat(archive): report health findings and use bound pair destinations | [bob-cli-j5.4.1.4](bob-cli-j5.4.1.4.md) | 2026-11-09 19:00:25 EST |
| bob-cli | [`03dfe6d`](https://github.com/bobs-org/bob-cli/commit/03dfe6deb86d6accfc825dc107136b198f5438be) | feat(collect-done): rename-following archive plan with link repair | [bob-cli-j5.4.1.5](bob-cli-j5.4.1.5.md) | 2026-11-09 19:50:15 EST |
| bob-cli | [`eba2bd5`](https://github.com/bobs-org/bob-cli/commit/eba2bd59a6fa6fdf8e827adbda1d42c03d97519b) | test(archive): cover stats attribution and Git commit across archive renames | [bob-cli-j5.4.1](bob-cli-j5.4.1.md) | 2026-11-09 20:28:56 EST |
| bob-cli | [`d65be1c`](https://github.com/bobs-org/bob-cli/commit/d65be1ce02b66f9a08c6a31049990aa74cccca65) | perf(archive): cache pair facts for read-only consumers | [bob-cli-j5.4.1](bob-cli-j5.4.1.md) | 2026-11-09 22:24:11 EST |
| bob-cli--plans | [`bob-cli--plans@60fec5c`](https://github.com/bobs-org/bob-cli--plans/commit/60fec5ca8562af388a55802c9d99427d292b97ca) | docs(plans): mark archive pairing plan done | [bob-cli-j5.4.1](bob-cli-j5.4.1.md) | 2026-11-09 22:24:47 EST |
| bob-cli | [`e5b0898`](https://github.com/bobs-org/bob-cli/commit/e5b0898e51670d39fe99fb959495ac7d12e37d3f) | feat(task-restore): add bob task restore over the task-move engine | [bob-cli-j5.6](bob-cli-j5.6.md) | 2026-11-09 23:34:10 EST |
| bob-cli | [`15a7999`](https://github.com/bobs-org/bob-cli/commit/15a79998ebee433dd2bd3dc76b1e3dc4c5ba0ab1) | feat(archive)!: keep window and group archived closures by month | [bob-cli-j5.5](bob-cli-j5.5.md) | 2026-11-10 00:03:43 EST |
| bob-cli | [`6a7afcd`](https://github.com/bobs-org/bob-cli/commit/6a7afcd2d9f7b5fa4b207e2687e75da97348f216) | feat(archive): treat only top-level done/ as the archive | [bob-cli-j5.7](bob-cli-j5.7.md) | 2026-11-10 01:01:21 EST |
| bob-plugins | [`bob-plugins@16c0454`](https://github.com/bobs-org/bob-plugins/commit/16c0454820f1d5034a7c2dc4062c42eb1f78f8ef) | feat(plugins): share one done/ path contract and reopen archived tasks via restore | [bob-cli-j5.8](bob-cli-j5.8.md) | 2026-11-10 01:14:11 EST |
| bob-cli | [`63ce765`](https://github.com/bobs-org/bob-cli/commit/63ce7653ad655251d2d44c2e48140dc135ca1565) | feat(archive)!: finish configurable keep-window behavior | [bob-cli-j5](README.md) | 2026-11-10 02:34:09 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-j5.6][1] | check epic phase statuses for restore dependencies | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.6/README.md

<!-- sase:referenced-by:end -->
