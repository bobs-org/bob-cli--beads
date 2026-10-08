# Bead: bob-cli-5k.5 — Build the Tasks JS sandbox only when a query needs it

[Bead Pages](../README.md) / [bob-cli-5k](README.md) / bob-cli-5k.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0y2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0y2.md) · **Assignee:** `bob-cli-5k.5` · **Size:** medium
**Created:** 2026-10-07 14:38:41 EDT · **Closed:** 2026-10-07 16:37:43 EDT
**Plan:** [202610/close\_top\_ten\_impact\_beads.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/close_top_ten_impact_beads.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | [bead:bob-cli-5o][1] | proposed by bob-cli-5k.5--2 notes #2/#3 |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-5o/README.md

<!-- sase:links:end -->

## Description

tasks-sandbox: construct the Tasks JavaScript sandbox lazily and give its initialization its own budget apart from the 2 s per-expression deadline, add regression tests, measure before/after latency on the live read path, and close bob-cli-33.

## Notes

[2026-10-07T20:37:43Z · bob-cli-5k.5] tasks-sandbox done on athena: JsSandbox now builds lazily via QueryAst::uses_javascript (filter/sort/group by-function) with init evals under a scaled init_timeout budget (10s base + 5ms/task, cap 120s) separate from the 2s per-expression deadline; all four query paths (query_matching_descriptions, query_rich_tasks, run, run_note) skip the sandbox otherwise. Verified: base fails live 'not done' query under load with init/interrupted, fixed tree exits 0 (494 tasks); by-function live query exits 0 (122 tasks). cargo fmt clean, clippy clean for touched files, lib 1905 pass, tasks/dataview/parity/cli freshness+plan+hooks suites pass, 9 new regression tests. Closed bob-cli-33.

[2026-10-07T21:28:30Z · bob-cli-5k.5--2] PROPOSED FOLLOW-UP: just check showed 3 flakes (capture kick timing + 2 bash completion readline tests) in the 21:02 run after a full pass at 20:39; all 3 pass on isolated retry — consider marking them flaky or quarantining timing-sensitive assertions

[2026-10-07T21:39:24Z · bob-cli-5k.5--2] PROPOSED FOLLOW-UP: just check flakes under full-suite parallel load, identical on phase tree and clean base (all 5 implicated tests pass isolated on both trees via stash comparison): 21:02 run failed capture-kick + 2 bash tests, latest run failed wikilink-timing (152ms budget) + vault task-completion instead, while the 20:39 full run was green. Consider raising the wikilink timing budget and quarantining the load-sensitive completion/capture tests

## Dependencies

- **Depends on:** [bob-cli-5k.3](bob-cli-5k.3.md) ✓ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5k.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-5k.5.md) | [bob-cli-5k.5](bob-cli-5k.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`577866d`](https://github.com/bobs-org/bob-cli/commit/577866d085ae7ea198a6745fca073154728c14dd) | feat(dataview): build Tasks JS sandbox only when query needs JavaScript | [bob-cli-5k.5](bob-cli-5k.5.md) | 2026-10-07 17:43:16 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5k.5--2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-5k.5.md

<!-- sase:referenced-by:end -->
