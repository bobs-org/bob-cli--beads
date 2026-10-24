# Bead: bob-cli-bj.3 — capture-complete relation\_label rows from the catalog

[Bead Pages](../README.md) / [bob-cli-bj](README.md) / bob-cli-bj.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2e.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2e.linker.w0.md) · **Assignee:** `bob-cli-bj.3` · **Size:** small
**Created:** 2026-10-24 13:34:45 EDT · **Closed:** 2026-10-24 16:07:19 EDT
**Plan:** [202610/relation\_label\_vocabulary.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_label_vocabulary.md)

## Description

label-complete: switch relation_label suggestions to the fast catalog, add key/inverse/existing/count/hidden fields and hidden_count, omit hidden rows, adopt the catalog spelling for case variants, fix the dedupe mismatch, and measure the latency budget.

## Notes

[2026-10-24T20:06:40Z · bob-cli-bj.3] Measured capture-complete on /home/bryan/bob with identical draft and cursor: installed baseline, 10 process runs, median 312.9 ms / p95 368.1 ms; new cache cold scan 1470.7 ms; warm snapshot, 10 runs, median 55.7 ms / p95 65.6 ms (budget <=150 ms). hyperfine is unavailable; timings used Python perf_counter around the process. Snapshot TTL is 60 seconds; successful capture writes invalidate immediately.

[2026-10-24T20:06:50Z · bob-cli-bj.3] PROPOSED FOLLOW-UP: Add the approved relation-label sentence to glossary:task-relation in the records phase; this phase followed memory_glossary=no.

[2026-10-24T20:06:56Z · bob-cli-bj.3] PROPOSED FOLLOW-UP: Make the planned label-rename phase invalidate relation-label snapshots after its vault-rewrite commit; current cache lasts 60 seconds, while capture commits already invalidate it.

[2026-10-24T20:07:02Z · bob-cli-bj.3] Verification: focused relation-label tests pass (13 matches), docs-check passes (447 passed, 1 skipped), fmt and clippy pass. Full tests expose clean-base failures: every_value_arg_has_a_decision (bob-cli-bc); CLI bash_strips_every_wordbreak_not_just_colon, named_start_after_inline_close_keeps_prefix, named_start_completes_after_hash, capture_complete_help_lists_options_alphabetically, and draft_related_stays_under_the_debug_perf_gate; current-load timing guards also failed in native capture-related and Pomodoro agenda tests. Clean-base reruns reproduced the themes check and the listed CLI failures.

[2026-10-24T20:07:19Z · bob-cli-bj.3] Catalog-backed relation-label completion, response fields, hidden filtering, canonical spelling, and cached latency are implemented. Focused relation tests, docs-check, fmt, and clippy pass; clean-base just-check failures are recorded in phase notes.

## Dependencies

- **Depends on:** [bob-cli-bj.2](bob-cli-bj.2.md) ✓ · ⧖ 2026-10-24
- **Blocks:** [bob-cli-bj.5](bob-cli-bj.5.md) ◐ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bj.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.3/README.md) | [bob-cli-bj.3](bob-cli-bj.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6def3ac`](https://github.com/bobs-org/bob-cli/commit/6def3ac88179c25ff6b54b4119c13c2875601ec8) | feat(capture-complete): use cached relation-label catalog | [bob-cli-bj.3](bob-cli-bj.3.md) | 2026-10-24 16:08:31 EDT |
