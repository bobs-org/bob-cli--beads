# Bead: bob-cli-fl.3.1 — Complete Stats clock selection and reporting

[Bead Pages](../README.md) / [bob-cli-fl.3](bob-cli-fl.3.md) / bob-cli-fl.3.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-fl.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fl.3.md) · **Assignee:** `bob-cli-fl.3.1.land`
**Created:** 2026-11-02 01:23:56 EST · **Closed:** 2026-11-02 04:52:10 EST
**Plan:** [202611/stats\_clock.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/stats_clock.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/stats_clock.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/stats_clock.md

<!-- sase:links:end -->

## Description

Finish bob-cli-fl.3 with Worked, Off-clock, and Total metrics, clock-aware session diagnostics, and complete CLI and JSON contracts.

## Notes

[2026-11-02T09:07:30Z · bob-cli-fl.3.1.land] FOLLOW-UP TRIAGE (before remaining-work tale): reviewed all three child beads and every note. fl.3.1.3 #1 (needless_borrow) and #2 (three grammar-5 assertions after grammar 6) are caused by active capture-list epic bob-cli-fn, specifically 0ebd0714 / fn.1; recorded both as DISCOVERED ISSUE on bob-cli-fn, no duplicate tasks. fl.3.1.3 #3 (duplicated journal_gap human warning) predates this epic: warning_lines is unchanged since 9be32d97 and appends metric warnings already present in report.warnings. Independently reproduced with the pre-clock workspace binary and confirmed current source/golden; filed small bug bob-cli-fr and marked ready. No proposals declined. The original parent phase fl.3 note #2 about a missing research artifact remains recorded for the outer fl lander; no dependency on that research was introduced here. New Stats diagnostic defects found in this landing remain epic work and will be in a medium tale, not follow-up tasks.

[2026-11-02T09:13:10Z · bob-cli-fl.3.1.land] LAND AUDIT: reviewed both approved plans and inherited DECISIONS, all 3 child beads and all notes, commits 4d950c58/4d2133b5/daf785b6, and actual Stats index/metrics/formula contexts/series/report/CLI/render/diagnostics source and tests. Lens, pinning, formulas, adoption, sub-shares, session filters, aliases, CSV, docs, and authorized glossary sentence are implemented. Integration covered 71a65dad and 0ebd0714 after first Stats commit, plus creation-window f171e3cc/62a82104/2d5ebfc9. Remaining epic work: homes.rs session_drifted skips empty lineups although the shared writer verdict says Worked/Unlinked; index_task_lines resolves fenced/frontmatter pseudo-tasks and can suppress real tasks via pseudo-duplicates; detect_overlaps partitions by note date and misses cross-midnight pairs from consecutive notes, and materializes every pair before its 50-entry cap. These are source-confirmed gaps requiring regression reproduction and repair, not task-bead follow-ups. Authored one medium tale to fix them and finish this epic and parent phase fl.3 in its final step. just check passed fmt, failed Clippy with exit 101 before tests (one denied error per lib target); no full-check run. No --epic-symbol entries exist for fl.3.1 or fl.3, and no just symvision recipe exists. Do not close yet or mark the plan done.

[2026-11-02T09:52:10Z · bob-cli-fl.3.1.land] LANDING COMPLETE: repaired clock diagnostics and verified the Stats clock epic.

Drift now uses the shared writer verdict on fully resolved counted Task Links, including empty Unlinked lineups (keyed off-clock empty rows drift; keyed Worked empty rows do not). Lookup uses ordinary vs embedded note_tasks scans over indexed buffers plus same-note Event Tasks, so frontmatter/fences/duplicates/global-filter and archived notes match the writers. Overlap is date-aware (overnight vs next-day early session), union-covered aggregate, 50-detail cap during the sweep, and additive schema-1 paths on cross-note pairs.

Verified: focused homes/compute/CLI Stats tests (including writer-to-Stats capture close), just check, just docs-check. No --epic-symbol entries. Parent phase fl.3 is next; outer bob-cli-fl stays for its lander. No memory changes.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fl.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fl.3.1.land.md) | [bob-cli-fl.3.1](bob-cli-fl.3.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2bf5e75`](https://github.com/bobs-org/bob-cli/commit/2bf5e759cef7c4d4fba364108a29225c01c4c585) | fix(stats): repair clock drift lookup and date-aware overlap | [bob-cli-fl.3.1](bob-cli-fl.3.1.md) | 2026-11-02 04:53:46 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fl.3.1.1][1] | Need parent epic DECISIONS and notes before implementing clock_evaluation | 1 |
| read-by | [agent:bob-cli-fl.3.1.2][2] | Need epic DECISIONS and child scope | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.3.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.3.1.2/README.md

<!-- sase:referenced-by:end -->
