# Bead: bob-cli-fs.4.1 — Finish capture relation successors for bob-cli-fs.4

[Bead Pages](../README.md) / [bob-cli-fs.4](bob-cli-fs.4.md) / bob-cli-fs.4.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-fs.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-fs.4.md) · **Assignee:** `bob-cli-fs.4.1.land`
**Created:** 2026-11-02 12:29:13 EST · **Closed:** 2026-11-02 18:56:49 EST
**Plan:** [202611/capture\_relation\_successors.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_relation_successors.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/capture_relation_successors.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | [bead:bob-cli-gc][2] | Measured while landing this epic; its relation-specific overhead stays with the epic's landing tale. |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_relation_successors.md
[2]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-gc/README.md

<!-- sase:links:end -->

## Description

Managed capture Done and parked gestures offer relation successors through the shared planner, with correct batch selection, generic bob-authored output, and verified read and latency budgets; bob-cli-fs.4 is completed and closed.

## Notes

[2026-11-02T23:11:06Z · bob-cli-fs.4.1.land] LAND TRIAGE (bob-cli-fs.4.1.land): No child phase recorded a PROPOSED FOLLOW-UP, so there were no proposals to accept or decline. Discovered follow-up not caused by this epic: the pre-feature !/x! close already misses the §12.7 70 ms and +5 ms dependents budgets (apollo baseline 8c7e7103: ! 219.87 ms median, dependents add +15.11 ms; athena, relations disabled: ! 95 ms vs hello 19 ms). Filed through /sase_new_task as bob-cli-gc (bug, large), linked related to this epic and to bob-cli-5v. Remaining epic work, caused by this epic: relation-enabled capture overhead. Athena release on a vault copy: x* 79->143 ms, ! with one source 96->143 ms, ! with no incoming relation 81->137 ms. Timers attribute about 35-40 ms of that to avoidable work: the retain-all-raw-bytes byte pass plus serial predicate rescans (+5 ms build, +5 ms from_raw), collect_relation_sources rebuilding the staged NoteIndex and cloning every LINKS note on each gesture (12 ms), and the whole dependency snapshot overlaid into note_texts so plan_successors does about 18 ms of extra work even with zero matched sources. Planning a tale to fix this and land.

[2026-11-02T23:56:49Z · bob-cli-fs.4.1.land--1] LAND tale relation_capture_overhead_landing: all six phases verified against source (snapshots, Done, parks, batches, presentation, SA coverage incl SA20 warning; sase bead epic-symbols clean at landing and rechecked clean). Integration: bob-cli-fs.3 authoring d8b4d4fb, merged-Pomodoro guards debee563, lineup restamping 37b2de64 are all ancestors of b4a17e86 and compatible. Perf tale (worker-side marker classification, no retain_raw rescan, cheap per-gesture source selection, narrowed engine source_texts) roughly halved overhead on apollo (8c7e7103 vs b4a17e86 plus perf tree 02bca984, 25 interleaved runs, 6847 md, 4.1G): x* park delta +189.93ms to +83.83ms (152.10/219.18 vs 235.93/321.82), ! Done delta +136.41ms to +67.32ms (183.62/232.28 vs 250.94/344.18), dependents add +12.76ms to -8.37ms (meets 5ms); hello/x medians meet 40ms. The 70ms !/x* budgets still miss on both binaries; that gap predates the epic and stays with bob-cli-gc, no budget declared met. Gates: just check exit 0 (fmt, clippy, workspace tests zero failures), just docs-check 447 passed 1 skipped, tiny-vault SA1 x* and SA4 ! human and JSON smokes ok. Triage: no PROPOSED FOLLOW-UP on any phase; no new task filed. just symvision has no recipe in this repo; epic-symbols is the clean symbol gate.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-fs.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-fs.4.1.land.md) | [bob-cli-fs.4.1](bob-cli-fs.4.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2aec2aa`](https://github.com/bobs-org/bob-cli/commit/2aec2aa472cf90d22ce607d3805dbceb10c92f72) | perf(capture): trim relation-successor overhead and re-measure apollo budgets | [bob-cli-fs.4.1](bob-cli-fs.4.1.md) | 2026-11-02 18:58:22 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fs.4.1.3][1] | Need parent epic scope and DECISIONS | 1 |
| read-by | [agent:bob-cli-fs.4.1.4][2] | Need epic decisions and earlier phase notes | 1 |
| read-by | [agent:bob-cli-fs.4.1.5][3] | Need epic DECISIONS that govern presentation | 3 |
| read-by | [agent:bob-cli-fs.4.1.land--1][4] | Confirm epic close state | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.4.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.4.1.4/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.4.1.5/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-fs.4.1.land.md

<!-- sase:referenced-by:end -->
