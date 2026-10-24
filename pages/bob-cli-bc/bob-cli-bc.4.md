# Bead: bob-cli-bc.4 — Recent themes in capture-complete

[Bead Pages](../README.md) / [bob-cli-bc](README.md) / bob-cli-bc.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2c.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2c.linker.w1.md) · **Assignee:** `bob-cli-bc.4` · **Size:** medium
**Created:** 2026-10-24 07:52:22 EDT · **Closed:** 2026-10-24 13:14:38 EDT
**Plan:** [202610/pomodoro\_themes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_themes.md)

## Description

suggest: compose today rows, recent themes, and the create row in both Pomodoro-name completion contexts, with lossless replacements and additive JSON.

## Notes

[2026-10-24T14:54:09Z · bob-cli-bc.4--3] PROPOSED FOLLOW-UP: Repair unrelated Highlights continuation scanner behavior — confirmed on clean HEAD f6f79099a6ca7a5c9f94b30c7e5280825a6331b8; both continuation_scan_reports_dangling_marker and continuation_scan_tucks_two_pages_and_is_idempotent fail identically.

[2026-10-24T15:09:29Z · bob-cli-bc.4--5] PT3 warm live-vault benchmarks (50 runs each): capture-complete p95 clean HEAD 74.287 ms, current 67.974 ms (−6.313 ms); capture-parse p95 clean HEAD 18.778 ms, current 19.118 ms (+0.341 ms).

[2026-10-24T16:29:43Z · bob-cli-bc.4] PROPOSED FOLLOW-UP: Trim the Mac Capture refs documentation budget — just docs-check reports docs/reference/mac-capture/refs.md at 6027 words against the 6000-word cap; the clean HEAD 8628ce2f snapshot reproduces the identical budget error. This phase changes only capture.md and pomodoro-themes.md.

[2026-10-24T16:29:50Z · bob-cli-bc.4] PROPOSED FOLLOW-UP: Stabilize timing-sensitive completion tests under concurrent load — completion::capture_text::named_start_completes_after_hash and named_start_after_inline_close_keeps_prefix returned no rows, and capture::related::draft_related_stays_under_the_debug_perf_gate took 1.2209s in the broad capture run; all three passed immediately on the identical compiled binary in isolated reruns (0.12s for both completion tests, 0.35s for the related test).

[2026-10-24T16:35:13Z · bob-cli-bc.4] Implementation now covers PT7 A/B/C/D/E composition in both completion contexts, PT8 lossless Recent/again replacements, additive metadata and zsh descriptions, shared menu/literal vectors, and docs. All new vector, hidden-theme acceptance, and dry-run round-trip tests pass. The earlier 50-run timing note predates this landed implementation and is being replaced with a fresh clean-HEAD comparison.

[2026-10-24T16:51:42Z · bob-cli-bc.4] PT3 verification after the final cache optimization: hyperfine 1.18, 5 warmups and 50 runs per command, debug binaries from clean HEAD 8628ce2f and this tree, read-only live vault with an isolated disposable XDG cache, draft =#bo. Nearest-rank p95 capture-complete: base 41.553ms, current 41.460ms (-0.093ms); capture-parse: base 19.541ms, current 19.496ms (-0.045ms). Completion means were 29.732ms / 36.364ms; hyperfine flagged baseline scheduling outliers. Both requested p95 deltas are within +5ms. Cache view reuses precomputed history totals, validates source/age/year/date fingerprints, and merges the already-read canonical live scan; area lookups are restricted to relevant theme keys.

[2026-10-24T17:04:31Z · bob-cli-bc.4] PROPOSED FOLLOW-UP: Declare completion kinds for themes rename positional arguments — full just check and a clean HEAD 8628ce2f snapshot both fail native::completion::kinds::tests::every_value_arg_has_a_decision identically with ["themes rename:old", "themes rename:new"]. This phase adds no CLI arguments.

[2026-10-24T17:05:01Z · bob-cli-bc.4] PROPOSED FOLLOW-UP: Review repeated completed-name ordering — the pre-existing today_start_rows deduplication replaces a repeated key in its first-seen vector slot before reversing; completed A, B, A therefore offers B before A. This phase preserves that Today ordering as required by PT7; a separate change can establish latest-occurrence ordering with a regression test.

[2026-10-24T17:06:31Z · bob-cli-bc.4] PROPOSED FOLLOW-UP: Corroboration for the existing Highlights continuation scanner follow-up — both continuation_scan_reports_dangling_marker (continuations.rs:313, uppercase Page 1) and continuation_scan_tucks_two_pages_and_is_idempotent (continuations.rs:218, zero continuations) fail identically on the current clean HEAD 8628ce2f snapshot and this tree. Full check passed 3344 library tests and 2006 CLI tests before the obsolete cache assertion was updated; all other integration targets passed.

[2026-10-24T17:14:21Z · bob-cli-bc.4] Final verification: PT7/PT8 shared menu and literal vectors, hidden-theme acceptance, cache invalidation, and all capture tests passed in the broad run. Updated read-only completion assertion passes with only the documented theme-cache files allowed. Regenerated CLI reference and its non-writing golden check pass. cargo fmt --check and git diff --check pass; full just check passed formatting/clippy and all other integration targets, with only the three clean-base failures documented above after correcting the cache assertion. Final just docs-check is green, including strict builds, links, search, executable tutorial, and 447 documentation tests (1 optional-dependency skip); the earlier mounted Mac refs budget failure is no longer present. No memory edits or CLI option changes.

[2026-10-24T17:14:38Z · bob-cli-bc.4] Implemented Recent-theme PT7 menus in both contexts, lossless PT8 replacements, additive JSON and zsh descriptions, shared vectors, and docs. Scope tests, corrected cache write protections, CLI reference check, formatting/clippy, and full docs-check passed. Live-vault 50-run p95 deltas: capture-complete -0.093ms; capture-parse -0.045ms, both within +5ms. Remaining full-gate failures are the three identically reproduced clean-base failures recorded as PROPOSED FOLLOW-UP. No epic-symbol entries remain.

## Dependencies

- **Depends on:** [bob-cli-bc.1](bob-cli-bc.1.md) ✓ · ⧖ 2026-10-24
- **Blocks:** [bob-cli-bc.10](bob-cli-bc.10.md) ✓ · ⧖ 2026-10-24
- **Depends on:** [bob-cli-bc.2](bob-cli-bc.2.md) ✓ · ⧖ 2026-10-24
- **Blocks:** [bob-cli-bc.7](bob-cli-bc.7.md) ✓ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bc.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bc.4/README.md) | [bob-cli-bc.4](bob-cli-bc.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2da7bbe`](https://github.com/bobs-org/bob-cli/commit/2da7bbef2ee00e27c0dba4420fc6d2b4a2c61b3a) | feat(capture): suggest recent themes with lossless names | [bob-cli-bc.4](bob-cli-bc.4.md) | 2026-10-24 13:16:00 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.2][1] | Identify the existing owner and task evidence for clean-base just check failures | 1 |
| read-by | [agent:bob-cli-bc.13][2] | Find the capture completion phase's PT3 measurements | 1 |
| read-by | [agent:bob-cli-bc.4][3] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-an.6.6.6.5.6.5.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bc.13/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bc.4/README.md

<!-- sase:referenced-by:end -->
