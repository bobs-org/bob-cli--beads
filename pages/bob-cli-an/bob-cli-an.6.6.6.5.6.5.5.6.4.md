# Bead: bob-cli-an.6.6.6.5.6.5.5.6.4 — Make the capture-related debug perf gate tolerate parallel test load

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6](bob-cli-an.6.6.6.5.6.5.5.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.4` · **Size:** small
**Created:** 2026-10-25 08:44:09 EDT · **Closed:** 2026-10-25 09:04:17 EDT
**Plan:** [202610/backlog\_batch9\_epipe\_listen\_publish\_refresh\_flakes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch9_epipe_listen_publish_refresh_flakes.md)

## Description

related-perf-gate: resolve bob-cli-bo by replacing the single cold 500 ms wall-clock sample with a load-tolerant measurement that still fails a real slowdown.

## Notes

[2026-10-25T13:04:05Z · bob-cli-an.6.6.6.5.6.5.5.6.4] Baseline: draft_related_stays_under_the_debug_perf_gate timed one cold debug bob capture-related run over a 40-note x 38-task fixture against 500 ms; reports show 330-667 ms isolated and 0.78-1.22 s under parallel just check. Fix (test-only, tests/cli/capture/related.rs): one untimed warmup of the big fixture plus a trivial one-task baseline vault, then 7 paired timed runs; gate is min(big-tiny) < 500 ms (same numeric budget, startup/load cancelled out) plus a gross min(big) < 2000 ms; failure message prints every sample. Slowdown probe: temporary +2 ms/candidate sleep in draft_related failed the gate as required (min diff 3.27 s, all samples listed) and was reverted; product code untouched. Tests: focused test passes; 3x cargo test --test cli -- --test-threads=64 at host load avg 15-28 all 2052 passed incl. the gate; just check EXIT=0 (3412 lib + 2052 cli + all integration suites, fmt+clippy clean). Target task bob-cli-bo left open for the lander.

[2026-10-25T13:04:17Z · bob-cli-an.6.6.6.5.6.5.5.6.4] Load-tolerant perf gate in tests/cli/capture/related.rs only: warmup + min of 7 paired runs vs trivial baseline, gate min(big-tiny) < 500 ms + gross min(big) < 2000 ms. Verified: deliberate +2 ms/candidate slowdown fails the gate (min diff 3.27 s) and was reverted; focused test passes; 3x full cargo test --test cli at --test-threads=64 under host load avg 15-28 all 2052 passed; just check EXIT=0 (3412 lib + 2052 cli, fmt+clippy clean). Target bob-cli-bo left open for the lander; no epic-symbols; no product-code or docs changes.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.4/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.4](bob-cli-an.6.6.6.5.6.5.5.6.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0e75ca5`](https://github.com/bobs-org/bob-cli/commit/0e75ca56901ff6f023416eb0b119d348d8aaf860) | test(capture): make related perf gate tolerate parallel load | [bob-cli-an.6.6.6.5.6.5.5.6.4](bob-cli-an.6.6.6.5.6.5.5.6.4.md) | 2026-10-25 09:05:07 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.4][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.4/README.md

<!-- sase:referenced-by:end -->
