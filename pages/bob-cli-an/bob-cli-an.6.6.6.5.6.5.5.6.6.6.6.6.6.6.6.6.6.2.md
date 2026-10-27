# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.2 — Shrink the live-vault bob stats index pass toward 300 ms

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.2` · **Size:** large
**Created:** 2026-10-27 11:12:34 EDT · **Closed:** 2026-10-27 13:03:24 EDT
**Plan:** [202610/backlog\_batch18\_hooks\_legacy\_key\_stats\_perf\_clippy\_gate\_refs\_copy\_docs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch18_hooks_legacy_key_stats_perf_clippy_gate_refs_copy_docs.md)

## Description

stats-perf: resolve bob-cli-6n per the stats_perf decision by profiling the single-pass stats index and cutting avoidable work without changing output.

## Notes

[2026-10-27T17:03:13Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.2--4] Stats performance phase closeout — source revision `b4a5850d32508eeb1133deab68444599d268e9db`.

Athena measurements used the release profile, read-only `~/bob`, `BOB_NOW=2026-10-11 12:00:00`, and `NO_COLOR=1`. The 5,354 Markdown files were read once in sorted order. Overview was 264.51 ms initial, 228.09 ms warm median (218.23–240.50, n=9); all metrics over 4w was 277.16 ms initial, 237.85 ms warm median (225.61–261.24, n=9). Temporary release-only timing counters were removed before verification. Five-run profiled medians: index pass 178.73 ms overview / 190.89 ms all metrics 4w; command wall time 243.03 / 256.85 ms.

Apollo used interleaved temporary baseline/final release copies, one initial plus nine warm runs per command, same clock/environment and read-only vault. Overview baseline: 666.05 / 345.99 ms (320.13–435.31); final: 427.37 / 345.16 ms (310.21–384.05). All metrics 4w baseline: 367.47 / 349.24 ms (307.65–478.03); final: 327.42 / 333.67 ms (303.16–422.46). Load averages were 5.5/7.6/10.4 before and 5.2/7.4/10.3 after. Apollo warm medians remain above 300 ms; its index-only stage was not profiled. No parser rewrite was retained.

Preserved baseline, rebuilt release, and final-copy binaries share SHA-256 `05c2d41622b13b454eba317385dbc39931c9f1e1c48a8e029a47129a1f52b3db`. On Athena, baseline-before/rebuilt-final/baseline-after JSON matched byte-for-byte for every input: live overview 246,785 bytes `a388d3916bd835c938e00d2c370e92297a4916468df574b3955582837ae81358`; worked comparison 161,011 bytes `06c3cf8f561707a76c7c05e4f158a172897ad9e5ce106474c292a1125ed6c584`; all metrics 4w 332,396 bytes `992df6218c91e9327c37ea2b31e756e71627a6681cf0eca84e9de53d22b44383`; stable fixture all metrics 4w 119,672 bytes `43132814e3f399e9eb266a31ac4927de05f982dd94b16b208db3a3e233467ae5`.

Verification passed: `cargo test --lib native::stats::` (176); `cargo test --test cli stats::` (13); release real-vault library parity (1, 275 ms); release real-vault CLI parity (1, worked comparison 246 ms); `just check` (full suite, fmt, clippy); `just docs-check` (447 passed, 1 skipped because font generation dependencies are absent); and `git diff --check`. The initial `just check` format failure was corrected and the complete verification rerun passed. The final docs record these measurements and host/load limitations in `docs/stats.md`. All vault reads were read-only.

[2026-10-27T17:03:24Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.2--4] Completed stats performance phase. Full evidence is in the preceding phase note: Athena measured index medians 178.73 ms (overview) and 190.89 ms (all metrics 4w); Athena and interleaved Apollo timing, matching binary and raw JSON hashes, focused/live-vault parity, just check, and just docs-check are recorded. Epic-symbol check was empty; parent epics remain open.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.2.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4a43170`](https://github.com/bobs-org/bob-cli/commit/4a43170b8103f2065a59b72fc25785abf96c60ca) | perf(stats): record current index measurements and parity | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.2.md) | 2026-10-27 13:04:13 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.2--4][1] | Need the assigned stats performance phase status and phase-specific closure criteria | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.2.md

<!-- sase:referenced-by:end -->
