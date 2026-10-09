# Bead: bob-cli-5w.1 — Lazy, shared, prefiltered vault snapshot for capture (bob-cli-5v)

[Bead Pages](../README.md) / [bob-cli-5w](README.md) / bob-cli-5w.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.0p.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.0p.linker.w0.md) · **Assignee:** `bob-cli-5w.1` · **Size:** medium
**Created:** 2026-10-09 11:54:15 EDT · **Closed:** 2026-10-09 12:23:13 EDT
**Plan:** [202610/successor\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/successor_links.md)

## Description

snapshot: in bob-cli, fix bead bob-cli-5v. Make DependencyContext lazy and resolve `!` and `&` notes from a walk-only index. Replace the full-vault recovery base with one batch-scoped, parallel, prefiltered dependents snapshot overlaid with staged text, and gate `!` recovery on `[id::]`. Output is unchanged apart from the documented gate edge. Ships guard tests and apollo timings.

## Notes

[2026-10-09T16:22:32Z · bob-cli-5w.1] Timings (apollo, release, temp copy of ~/bob excl .git/.obsidian, 6211 .md files, BOB_NOW 2026-10-09, 7 dry runs each, warm page cache). hello: 6-7ms (before 220-270ms, target <=40ms OK). =x successful close completing nothing: 6-8ms (before 280ms, target <=40ms OK). !sase:fix-apollo (gate passes, real dependent sase__re-launch-apollo-agents recovered [?]->[ ]): 135-162ms (before 370-410ms, well under ~400ms OK; the 70ms epic target is 5w.3 capture_complete work). Intended commit message records the gate edge: dependents naming only the canonical id (note__block) of a target without [id::] no longer recover at close time; the hooks heal them on the next run.

[2026-10-09T16:22:41Z · bob-cli-5w.1] PROPOSED FOLLOW-UP: record "a closed planned task hands its slot to its successors" as a decisions strand (epic auto-decision decision_record=no)

[2026-10-09T16:22:46Z · bob-cli-5w.1] PROPOSED FOLLOW-UP: add a "Successor Link" glossary term (epic auto-decision glossary_term=no)

[2026-10-09T16:22:50Z · bob-cli-5w.1] PROPOSED FOLLOW-UP: fix 9 pre-existing highlights_ref::return_links filter_* lib test failures that reproduce identically on the clean base tree (verified via stash; unrelated to this phase)

[2026-10-09T16:23:13Z · bob-cli-5w.1] Verified: cargo fmt clean; clippy exit 0 (only pre-existing warnings); lib capture 853 + equivalence test pass; cli capture 521 pass incl 3 new guards; other integration targets pass; full just check has only 9 pre-existing highlights_ref return_links failures identical on base (recorded as follow-up). Apollo release timings 7x dry-run: hello 6-7ms, =x 6-8ms, !sase:fix-apollo 135-162ms with live recovery of the real dependent. No epic-symbols left. Work uncommitted for land-agent review.

## Dependencies

- **Blocks:** [bob-cli-5w.3](bob-cli-5w.3.md) ◐ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5w.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5w.1/README.md) | [bob-cli-5w.1](bob-cli-5w.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e190a7d`](https://github.com/bobs-org/bob-cli/commit/e190a7dc84e74ff2e58abae96405edc0be4727c9) | perf(capture): lazy vault snapshot for capture batches | [bob-cli-5w.1](bob-cli-5w.1.md) | 2026-10-09 12:24:26 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5w.1][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5w.1/README.md

<!-- sase:referenced-by:end -->
