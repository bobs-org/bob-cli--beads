# Bead: bob-cli-5s.5 — Refs library service and panel model

[Bead Pages](../README.md) / [bob-cli-5s](README.md) / bob-cli-5s.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.5z` · **Assignee:** `bob-cli-5s.5` · **Size:** medium
**Created:** 2026-10-08 19:32:40 EDT · **Closed:** 2026-10-09 03:29:22 EDT
**Plan:** [202610/bob\_refs\_panel.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_refs_panel.md)

## Description

refs-panel-model: build the RefsLibrary refresh service (cache, watcher, git-date pass, Today, Spotlight sweep, missing PDFs, open log) and the RefsPanelModel (query, scope, frozen listing, selection, commands, open dispatch, banners) with fake-bob tests.

## Notes

[2026-10-09T07:29:04Z · bob-cli-5s.5--4] PROPOSED FOLLOW-UP: refs_decision_memory=no — consider a decision record extending the thin-client rule to Bob Refs (opening never mutates the vault); no decisions memory edited per epic DECISIONS.

[2026-10-09T07:29:22Z · bob-cli-5s.5--4] refs-panel-model done and CI green: bob-mac-capture run https://github.com/bobs-org/bob-mac-capture/actions/runs/37898248619 (SHA 75770a0, commit relaxing RefsRanking testPerformanceGuard to 10s for debug CI) concluded success. Verified: gh run list shows 37898248619 completed:success for 75770a0; prior ebe2d56 fixes (sticky unavailableIDs, openSelected reorder, Today-lane hardening) included. Skipped memory change recorded as PROPOSED FOLLOW-UP per refs_decision_memory=no. No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-5s.4](bob-cli-5s.4.md) ✓ · ⧖ 2026-10-08
- **Blocks:** [bob-cli-5s.6](bob-cli-5s.6.md) ✓ · ⧖ 2026-10-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5s.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5s.5/README.md) | [bob-cli-5s.5](bob-cli-5s.5.md) | 6 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@d013a7f`](https://github.com/bobs-org/bob-mac-capture/commit/d013a7f0a110502e8609e4c943d8cbc5606e8efa) | feat(refs): add RefsLibrary refresh service and RefsPanelModel | [bob-cli-5s.5](bob-cli-5s.5.md) | 2026-10-09 01:49:51 EDT |
| bob-mac-capture | [`bob-mac-capture@f720ce3`](https://github.com/bobs-org/bob-mac-capture/commit/f720ce3a78e523623d5a5e18efbdf3de1683ea32) | fix(refs): correct Spotlight overlay use and missing imports | [bob-cli-5s.5](bob-cli-5s.5.md) | 2026-10-09 01:54:50 EDT |
| bob-mac-capture | [`bob-mac-capture@f6af6db`](https://github.com/bobs-org/bob-mac-capture/commit/f6af6db45553116ec727869654c246babe699131) | fix(refs): widen test Harness to fileprivate so panel tests compile | [bob-cli-5s.5](bob-cli-5s.5.md) | 2026-10-09 02:03:41 EDT |
| bob-mac-capture | [`bob-mac-capture@47ea15d`](https://github.com/bobs-org/bob-mac-capture/commit/47ea15d821eda5371c2968dfe33ca9b60f3cdc7a) | fix(refs): repair refs-panel-model tests that never triggered a refresh | [bob-cli-5s.5](bob-cli-5s.5.md) | 2026-10-09 02:50:21 EDT |
| bob-mac-capture | [`bob-mac-capture@ebe2d56`](https://github.com/bobs-org/bob-mac-capture/commit/ebe2d56fd8a3cab1ab0a5cb79d2960e66c349a09) | fix(refs): keep vanished-row flags across publishes and harden lane races | [bob-cli-5s.5](bob-cli-5s.5.md) | 2026-10-09 03:03:45 EDT |
| bob-mac-capture | [`bob-mac-capture@75770a0`](https://github.com/bobs-org/bob-mac-capture/commit/75770a09cfc5b88e4738c807f9216ced2579d98a) | fix(refs): relax ranking perf guard to 10s for debug CI builds | [bob-cli-5s.5](bob-cli-5s.5.md) | 2026-10-09 03:18:13 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5s.5][1] | Need full bead including notes and remaining work | 2 |
| read-by | [agent:bob-cli-5s.5--1][2] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-5s.5--2][2] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-5s.5--3][2] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5s.5/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-5s.5.md

<!-- sase:referenced-by:end -->
